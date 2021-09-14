---
description: El método SpliceWithNext une el objeto de origen a otro objeto de origen.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: Método IAMTimelineSrc::SpliceWithNext (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891921"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>IamTimelineSrc::SpliceWithNext (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SpliceWithNext` método une el objeto de origen a otro objeto de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNext* 
</dt> <dd>

Puntero a la [**interfaz IAMTimelineObj**](iamtimelineobj.md) del objeto de origen que se unirá al origen actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los posibles valores devueltos se incluyen los siguientes:



| Código devuelto                                                                                   | Descripción                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>                                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | El objeto especificado por *el parámetro pNext* no es un objeto de origen.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL.<br/>                                    |



 

## <a name="remarks"></a>Observaciones

Como se implementa actualmente, este método descarta los efectos en *pNext*.

Para que este método se realice correctamente, *pNext* debe ser un marco de coincidencia del objeto de origen actual, definido de la siguiente manera:

-   Debe compartir el mismo archivo de código fuente.
-   La hora de inicio del medio debe ser igual a la hora de detenerse del origen actual.
-   La velocidad de reproducción debe ser la misma. La velocidad de reproducción es la duración de los medios dividida por la duración de la escala de tiempo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




