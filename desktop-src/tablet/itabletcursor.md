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
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913301"
---
# <a name="itabletcursor-interface"></a>Interfaz ITabletCursor

Representa un objeto de lápiz óptico.

## <a name="members"></a>Miembros

La interfaz **ITabletCursor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITabletCursor** tiene estos métodos.



| Método                                                 | Descripción                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetButton**](itabletcursor-getbutton.md)           | Recupera el objeto de botón especificado de un lápiz de Tablet PC.<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | Recupera el número de botones del lápiz de Tablet PC.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Recupera el identificador del lápiz óptico.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Recupera el nombre del lápiz de Tablet PC.<br/>                    |
| [**IsInverted**](itabletcursor-isinverted.md)         | Indica si el lápiz está en la parte inferior.<br/>                     |



 

## <a name="remarks"></a>Observaciones

No utilice esta interfaz.

En el código siguiente se describe cómo se define la interfaz **ITabletCursor** .

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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

