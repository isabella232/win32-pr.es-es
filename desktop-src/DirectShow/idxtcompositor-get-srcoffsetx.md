---
description: El método \_ get SrcOffsetX recupera el desplazamiento horizontal del rectángulo de origen.
ms.assetid: 528a5306-86bd-4ae2-ad03-57247362c5b5
title: Método IDxtCompositor::get_SrcOffsetX (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b66748c9c7114659d410558b2931bc64e9f3bd41b1e62b7fa265ae166a91d6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427985"
---
# <a name="idxtcompositorget_srcoffsetx-method"></a>IDxtCompositor::get \_ SrcOffsetX (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_SrcOffsetX` método recupera el desplazamiento horizontal del rectángulo de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SrcOffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el desplazamiento horizontal del rectángulo de origen, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDxtCompositor (interfaz)**](idxtcompositor.md)
</dt> </dl>

 

 




