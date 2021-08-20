---
description: El método SetMediaTimes establece las horas de detenerse e iniciar los medios.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: Método IAMTimelineSrc::SetMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5de058e31da605b96f7b013c03e9c0d020daa11ec676618b4a13f5ff92e701f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154934"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>Método IAMTimelineSrc::SetMediaTimes

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMediaTimes` método establece las horas de detención e inicio de los medios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de inicio del medio, en unidades de 100 nanosegundos.

</dd> <dt>

*Detención* 
</dt> <dd>

Tiempo de detención de medios, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Las horas de medios son las horas de detenerse e iniciar con respecto al archivo multimedia original. Establezca siempre las horas multimedia cuando agregue un origen de audio o vídeo a la escala de tiempo. De lo contrario, podrían producirse problemas de representación. La hora de detenerse debe ser mayor que la hora de inicio.

Para usar un fotograma de un origen de vídeo, establezca la hora de detenerse en una cantidad fraccionria mayor que la hora de inicio, como 100 nanosegundos. Si se establece en el mismo valor, se produce un error de representación.

Si la duración de la escala de tiempo no coincide con la duración del medio, el origen se extiende o reduce en consecuencia. Esto hace que el clip se reprodgue más lento o más rápido que la velocidad de creación. (El cambio de tono se producirá en un origen de audio). Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Puede especificar la duración del archivo de origen llamando al [**método SetMediaLength.**](iamtimelinesrc-setmedialength.md) Si establece un tiempo de detención de medios que supera la duración, DES trunca la hora de detenerse.

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

 

 




