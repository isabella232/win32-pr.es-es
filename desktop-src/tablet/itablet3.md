---
description: La interfaz ITablet3 permite realizar consultas multitouch para la entrada.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interfaz ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449848"
---
# <a name="itablet3-interface"></a>Interfaz ITablet3

La interfaz ITablet3 permite realizar consultas multitouch para la entrada.

## <a name="members"></a>Miembros

La **interfaz ITablet3** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet3 también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITablet3** tiene estos métodos.



| Método                                                  | Descripción                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Recupera el número máximo de entradas admitidas.<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | Indica si multitouch está habilitado para este objeto.<br/> |



 

## <a name="remarks"></a>Comentarios

Los desarrolladores no deben usar esta interfaz

En el código siguiente se describe cómo se define la interfaz **ITablet3.**

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

