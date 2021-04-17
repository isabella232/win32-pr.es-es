---
description: El método SetMediaTimes establece las horas de detención e inicio del medio.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'IAMTimelineSrc:: SetMediaTimes (método) (QEDIT. h)'
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
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680568"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a>IAMTimelineSrc:: SetMediaTimes (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetMediaTimes` método establece las horas de detención e inicio del medio.

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

Hora de inicio del medio, en unidades de 100-nanosegundos.

</dd> <dt>

*Detención* 
</dt> <dd>

Tiempo de detención del medio, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las horas de los medios son las horas de detención e inicio relativas al archivo multimedia original. Establezca siempre las horas del medio al agregar un origen de vídeo o de audio a la escala de tiempo. De lo contrario, podrían producirse problemas de representación. La hora de detención debe ser mayor que la hora de inicio.

Para usar un fotograma fijo de un origen de vídeo, establezca la hora de detención en una cantidad fraccionaria superior a la hora de inicio, por ejemplo, 100 nanosegundos. Si se establecen en el mismo valor, se produce un error de representación.

Si la duración de la escala de tiempo no coincide con la duración del medio, el origen se expande o se reduce en consecuencia. Esto hace que el clip se reproduzca más lentamente o más rápido que la tarifa creada. (El cambio de tono se producirá en un origen de audio). Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Puede especificar la duración del archivo de código fuente llamando al método [**SetMediaLength**](iamtimelinesrc-setmedialength.md) . Si establece una hora de detención de medios que supera la duración, DES trunca la hora de detención.

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

 

 




