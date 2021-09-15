---
description: Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.
title: Interfaz IShellFolderSearchableCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579553"
---
# <a name="ishellfoldersearchablecallback-interface"></a>Interfaz IShellFolderSearchableCallback

Expone rutinas de devolución de llamada para supervisar el proceso de búsqueda.

## <a name="members"></a>Members

La **interfaz IShellFolderSearchableCallback** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IShellFolderSearchableCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IShellFolderSearchableCallback** tiene estos métodos.



| Método                                                      | Descripción                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [**RunBegin**](ishellfoldersearchablecallback-runbegin.md) | Indica que se inició una búsqueda.<br/>  |
| [**RunEnd**](ishellfoldersearchablecallback-runend.md)     | Indica que ha finalizado una búsqueda.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz no se define en ningún archivo de encabezado público. Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
