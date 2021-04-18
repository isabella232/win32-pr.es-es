---
description: El método SetStreamNumber especifica la secuencia que se va a leer del archivo de código fuente asociado a este objeto de origen.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'IAMTimelineSrc:: SetStreamNumber (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690612"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>IAMTimelineSrc:: SetStreamNumber (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetStreamNumber` método especifica la secuencia que se va a leer del archivo de código fuente asociado a este objeto de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Val* 
</dt> <dd>

El número de secuencia, desde el conjunto de secuencias que coinciden con el tipo de medio del grupo primario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El parámetro *Val* especifica un número de secuencia del conjunto de secuencias que coincide con el tipo de medio del grupo primario, no del conjunto completo de secuencias del archivo de código fuente. Por ejemplo, supongamos que un archivo contiene dos secuencias de vídeo y dos secuencias de audio. Si el objeto de origen está dentro de un grupo de vídeos, al establecer *Val* en 0, se selecciona la primera secuencia de vídeo. El autor de la llamada es responsable de especificar un número de secuencia válido.

El valor predeterminado del número de secuencia es cero.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




