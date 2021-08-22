---
description: Especifica el tamaño del segmento en unidades de megabyte (MB), bits o fila de MB.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d068d8b2c5fc15fdb82c3ffe068e6926d28228a19367114067e02ebc44b03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035353"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>Propiedad CODECAPI \_ AVEncSliceControlSize

Especifica el tamaño del segmento en unidades de megabyte (MB), bits o fila de MB.

## <a name="data-type"></a>Tipo de datos

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>Comentarios

**Codificadores H.264/AVC:**

El significado del valor de CODECAPI AVEncSliceControlSize se controla mediante la propiedad \_ [CODECAPI \_ AVEncSliceControlMode.](codecapi-avencslicecontrolmode.md) En la tabla siguiente se muestra cómo las propiedades CODECAPI \_ AVEncSliceControlSize y CODECAPI AVEncSliceControlMode controlan el tamaño y el número de segmentos de \_ un fotograma.



| Configuración de \_ CODECAPI AVEncSliceControlMode | Significado del valor                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Se trata de un entero que indica el tamaño de cada segmento del marco en unidades de macrobloqueos. <br/> El codificador debe rechazar la configuración cuando el valor sea mayor que el número de macrobloqueos del marco.<br/>                                                                                                                                                                         |
| 1                                       | Se trata de un entero que indica el tamaño de cada segmento del marco en unidades de bits. <br/> El codificador debe iniciar un nuevo segmento en el macrobloqueo que hace que el número de bits del segmento supere este valor (por lo que el tamaño de cada segmento siempre será menor o igual que este valor). Esto significa que el último tamaño de segmento podría ser significativamente menor que este valor. <br/> |
| 2                                       | Se trata de un entero que indica el tamaño de cada segmento del marco en unidades de filas de macrobloqueo. <br/> El codificador debe rechazar la configuración cuando el valor sea mayor que el número de filas de macrobloqueo en el marco.<br/>                                                                                                                                                                 |



 

Si la aplicación no establece un valor para [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), el codificador debe devolver un error.

El valor predeterminado recomendado es tener un solo segmento para todo el marco.

Algunos codificadores pueden codificar segmentos en paralelo, por lo que el rendimiento podría verse afectado en función de la configuración del control de segmento. Por ejemplo, codificar un fotograma como un solo segmento podría ser más lento que si el marco se codificase como varios segmentos.

La configuración del control de segmento es dinámica y se puede cambiar durante la sesión de codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




