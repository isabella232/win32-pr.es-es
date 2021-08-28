---
description: El método \_ get MaskNum recupera el código de borrado SMPTE del borrado.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: Método IDxtAsynceg::get_MaskNum (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9265cac204609381e5d3d6d58d4fbd697f623913098e1f9ebe50d891db31b850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131045"
---
# <a name="idxtjpegget_masknum-method"></a>IDxt Maskeg::get \_ MaskNum (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_MaskNum` método recupera el código de borrado SMPTE del borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el código de borrado de SMPTE. Para obtener una lista de borrados de SMPTE admitidos, vea [Transición de borrado de SMPTE.](smpte-wipe-transition.md)

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

[**IDxt Jpeg (interfaz)**](idxtjpeg.md)
</dt> </dl>

 

 




