---
description: Representa un objeto de lápiz óptico.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interfaz ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 83a24329b318ec2bb542a3bbb63a28d4db9fce877b99f75aa7091670825fa439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716943"
---
# <a name="itabletcursor-interface"></a>Interfaz ITabletCursor

Representa un objeto de lápiz óptico.

## <a name="members"></a>Miembros

La **interfaz ITabletCursor** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletCursor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITabletCursor** tiene estos métodos.



| Método                                                 | Descripción                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetButton**](itabletcursor-getbutton.md)           | Recupera el objeto de botón especificado de un lápiz óptico de tableta.<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | Recupera el número de botones del lápiz óptico de la tableta.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Recupera el identificador del lápiz óptico.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Recupera el nombre del lápiz óptico de tableta.<br/>                    |
| [**IsInverted**](itabletcursor-isinverted.md)         | Indica si el lápiz óptico está al revés.<br/>                     |



 

## <a name="remarks"></a>Comentarios

No utilice esta interfaz.

En el código siguiente se describe cómo se define la interfaz **ITabletCursor.**

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

