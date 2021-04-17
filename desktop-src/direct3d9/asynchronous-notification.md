---
description: Hay un número de consultas interesantes en un controlador que una aplicación puede realizar si no hay ningún costo de rendimiento.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notificación asincrónica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705313"
---
# <a name="asynchronous-notification-direct3d-9"></a>Notificación asincrónica (Direct3D 9)

Hay un número de consultas interesantes en un controlador que una aplicación puede realizar si no hay ningún costo de rendimiento. En Direct3D 7 y Direct3D 8, un mecanismo de consulta sincrónico, GetInfo, funcionó bien para cosas como las estadísticas, pero no se agregaron consultas críticas para el rendimiento. Hay otras cosas (como barreras) que son intrínsecamente asincrónicas. Se trata de una API sencilla para realizar consultas sincrónicas y asincrónicas. Las GetInfo se retirarán en Direct3D 9.

Cree una consulta mediante [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api). Este método toma un D3DQUERYTYPE, que define el tipo de consulta que se va a realizar y devuelve un puntero a un objeto [**IDirect3DQuery9**](/windows/desktop/api) . Si no se admite el tipo de consulta, la llamada devuelve un error D3DERR \_ NOTAVAILABLE. Mediante el objeto de consulta, la aplicación envía la consulta al tiempo de ejecución mediante [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)y sondea el estado de la consulta mediante [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Si el resultado de la consulta está disponible, \_ se devuelve un valor correcto; de lo contrario, \_ se devuelve s. Se espera que la aplicación pase un búfer de tamaño adecuado para los resultados de la consulta.

La aplicación tiene una opción para obligar al tiempo de ejecución a vaciar la consulta hasta el controlador mediante el \_ vaciado de D3DGETDATA con [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata). Provoca un vaciado, forzando al controlador a ver la consulta. En este caso, \_ se devuelve D3DERR DEVICELOST si se pierde el dispositivo.

Todas las consultas se pierden cuando se pierde el dispositivo, la aplicación tiene que volver a crearlas. Si el dispositivo no admite la consulta y el valor de pQueryID es **null**, se producirá un error en la creación de la consulta con D3DERR \_ INVALIDCALL.

En la tabla siguiente se resume información importante acerca de cada tipo de consulta.



| QuertyType                    | Marca de problema válida              | Búfer GetData              | Tiempo de ejecución      | Inicio implícito de la consulta |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | Final de D3DISSUE \_                 | D3DDEVINFO \_ VCACHE          | Venta directa/depuración | CreateDevice                |
| D3DQUERYTYPE \_ ResourceManager | Final de D3DISSUE \_                 | D3DDEVINFO \_ ResourceManager | Solo depuración   | Presente                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | Final de D3DISSUE \_                 | D3DDEVINFO \_ D3DVERTEXSTATS  | Solo depuración   | Presente                     |
| \_Evento D3DQUERYTYPE           | Final de D3DISSUE \_                 | BOOL                        | Venta directa/depuración | CreateDevice                |
| Oclusión de D3DQUERYTYPE \_       | D3DISSUE \_ Begin, D3DISSUE \_ End | DWORD                       | Venta directa/depuración | N/D                         |



 

Campo Flags para [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



Campo Flags para [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
