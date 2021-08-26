---
description: El método SetStreamNumber especifica qué secuencia se va a leer del archivo de origen asociado a este objeto de origen.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: Método IAMTimelineSrc::SetStreamNumber (Qedit.h)
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
ms.openlocfilehash: ae313121831dc2855a2f07ba3c7727e87736b77a8c5f98078d2237bb9520cf6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982965"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>IamTimelineSrc::SetStreamNumber (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetStreamNumber` método especifica qué secuencia se va a leer del archivo de origen asociado a este objeto de origen.

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

Número de secuencia del conjunto de secuencias que coinciden con el tipo de medio del grupo primario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El *parámetro Val* especifica un número de secuencia del conjunto de secuencias que coincide con el tipo de medio del grupo primario, no de todo el conjunto de secuencias del archivo de origen. Por ejemplo, supongamos que un archivo contiene dos secuencias de vídeo y dos secuencias de audio. Si el objeto de origen está dentro de un grupo de vídeo, si se establece *Val* en 0, se selecciona la primera secuencia de vídeo. El autor de la llamada es responsable de especificar un número de secuencia válido.

El valor predeterminado del número de secuencia es cero.

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




