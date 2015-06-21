```csharp
public interface IDataContext
{
	IQueryable<T> All<T>() where T : class;
    IQueryable<T> Find<T>(Expression<Func<T, bool>> predicate) where T : class;
    T GetOne<T>(Expression<Func<T, bool>> predicate) where T : class;
    T Add<T>(T entity) where T : class;
    T Update<T>(T entity) where T : class;
    T Remove<T>(T entity) where T : class;
    bool SaveChanges();
}
```
