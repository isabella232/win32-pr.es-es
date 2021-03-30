---
description: Representa información general sobre un botón en un dispositivo de lápiz óptico.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interfaz ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360972"
---
# <a name="itabletcursorbutton-interface"></a>Interfaz ITabletCursorButton

Representa información general sobre un botón en un dispositivo de lápiz óptico.

## <a name="members"></a>Miembros

La interfaz **ITabletCursorButton** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursorButton** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITabletCursorButton** tiene estos métodos.



| Método                                         | Descripción                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Recupera el identificador único del botón del lápiz óptico.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Recupera el nombre del botón del lápiz óptico.<br/>              |



 

## <a name="remarks"></a>Observaciones

Los desarrolladores no deben utilizar esta interfaz.

En el código siguiente se muestra cómo se define la interfaz **ITabletCursorButton** .

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

