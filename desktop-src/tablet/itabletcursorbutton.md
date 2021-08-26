---
description: Representa información general sobre un botón en un dispositivo de lápiz óptico.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: ITabletCursorButton (interfaz)
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
ms.openlocfilehash: 76f5e581a4db81d9e260b388cc129d915121a69f3b360441e4220fd58aa0e623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938605"
---
# <a name="itabletcursorbutton-interface"></a>ITabletCursorButton (interfaz)

Representa información general sobre un botón en un dispositivo de lápiz óptico.

## <a name="members"></a>Miembros

La **interfaz ITabletCursorButton** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletCursorButton** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITabletCursorButton** tiene estos métodos.



| Método                                         | Descripción                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Recupera el identificador único del botón de lápiz óptico.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Recupera el nombre del botón del lápiz óptico.<br/>              |



 

## <a name="remarks"></a>Comentarios

Los desarrolladores no deben usar esta interfaz.

El código siguiente muestra cómo se define la interfaz **ITabletCursorButton.**

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
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletCursorButton (Interfaz)**](itabletcursorbutton.md)
</dt> </dl>

 

