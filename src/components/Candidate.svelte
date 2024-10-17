<script>
export let name;
export let title;
export let src;
</script>

<article>
  <img src={src} alt={name}>
  <div>
  <hgroup>
    <h1>{name}</h1>
    <p>for {title}</p>
  </hgroup>
  <slot></slot>
  <!-- TODO address tag -->
  </div>
</article>

<style>
  article {
    display: flex;
    width: 36.625rem;
    align-items: center;
    gap: 1.1175rem;
    flex-shrink: 0;
    
    & img {
      border-radius: 8.2rem;
      width: 8rem;
      height: 8rem;
      flex-shrink: 0;
      object-fit: cover;
    }
    
    & div {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 0.5rem;
      flex: 1 0 0;
      
      & hgroup {
        gap: 0.5rem;
        & h1 {
          leading-trim: both;
          text-edge: cap;
          font-size: 2rem;
          font-style: normal;
          font-weight: 600;
          line-height: normal;
          letter-spacing: -0.10106rem;
        }
        
        & p {
          leading-trim: both;
          text-edge: cap;
          font-size: 1.5rem;
          font-style: normal;
          font-weight: 500;
          line-height: normal;
          letter-spacing: -0.06706rem;
        }
      }
      
      & p {
        leading-trim: both;
        text-edge: cap;
        font-size: 1.25rem;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
        letter-spacing: -0.05rem;
      }
    }
  }
</style>