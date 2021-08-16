---
description: Expone métodos que permiten a una carpeta de Shell admitir vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).
title: Interfaz IShellFolderViewType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: 30722e32a555b386e166e5525e0d4361dbe9d9bc6a58051e4727c661ebe49073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714125"
---
# <a name="ishellfolderviewtype-interface"></a>Interfaz IShellFolderViewType

Expone métodos que permiten a una carpeta de Shell admitir vistas diferentes en su contenido (diferentes diseños jerárquicos de sus datos).

## <a name="members"></a>Miembros

La **interfaz IShellFolderViewType** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IShellFolderViewType** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IShellFolderViewType** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumViews**](ishellfolderviewtype-enumviews.md)                         | Recupera un enumerador que devolverá un PIDL para cada vista extendida.<br/>                                                                                |
| [**GetDefaultViewName**](ishellfolderviewtype-getdefaultviewname.md)       | Obtiene el nombre de la vista predeterminada. Llame [**a IShellFolder::GetDisplayNameOf para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) recuperar los nombres de las otras vistas.<br/> |
| [**GetViewTypeProperties**](ishellfolderviewtype-getviewtypeproperties.md) | Obtiene las propiedades de la vista.<br/>                                                                                                                          |
| [**TranslateViewPidl**](ishellfolderviewtype-translateviewpidl.md)         | Reconstruye un PIDL de una representación jerárquica de la carpeta Shell en una representación diferente.<br/>                                             |



 

## <a name="remarks"></a>Comentarios

Este enumerador devuelve PIDL que son carpetas ocultas especiales en el nivel superior de la carpeta Shell, que de lo contrario no se enumeran. La vista predeterminada es la que la carpeta shell muestra con normalidad.

Esta interfaz no está definida en ningún archivo de encabezado público. Si decide implementar esta interfaz, puede usar el siguiente código de C/C++ para declarar sus métodos.


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderViewType Methods ***

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList **ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
