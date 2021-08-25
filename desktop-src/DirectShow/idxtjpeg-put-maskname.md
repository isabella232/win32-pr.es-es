---
description: El método put MaskName especifica el nombre de un \_ archivo JPEG que se usará como máscara de borrado.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: Método IDxt Maskeg::p ut_MaskName (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7a43398020c49f2a6dab1cd56fc0244c4be88e2e45e38e0f6bd63c119bbf66a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755945"
---
# <a name="idxtjpegput_maskname-method"></a>Método MaskName :p \_ IDxtAsynceg::p ut

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método especifica el nombre de un archivo JPEG que `put_MaskName` se usará como máscara de borrado. Esta máscara se usará en lugar de una de las máscaras de borrado integradas. El archivo debe contener un degradado monocromo de 8 bits por píxel. El degradado se usa como máscara para definir la progresión del borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Especifica el nombre del archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Para revertir a una máscara integrada, establezca la **propiedad MaskNum.**

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
</dt> <dt>

[**IDxt Maskeg::p ut \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




