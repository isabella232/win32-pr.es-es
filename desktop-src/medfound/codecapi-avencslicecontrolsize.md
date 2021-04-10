---
description: Especifica el tamaño del segmento en unidades de megabytes (MB), bits o una fila de MB.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Propiedad CODECAPI_AVEncSliceControlSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153676"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>\_Propiedad AVEncSliceControlSize de CODECAPI

Especifica el tamaño del segmento en unidades de megabytes (MB), bits o una fila de MB.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>Observaciones

**Codificadores H. 264/AVC:**

El significado del valor de CODECAPI \_ AVEncSliceControlSize se controla mediante la propiedad [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) . En la tabla siguiente se muestra cómo las \_ propiedades CODECAPI AVEncSliceControlSize y CODECAPI \_ AVEncSliceControlMode controlan el tamaño y el número de segmentos de un marco.



| Configuración de CODECAPI \_ AVEncSliceControlMode | Significado del valor                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Es un entero que indica el tamaño de cada sector del marco en unidades de macrobloques. <br/> El codificador debe rechazar la configuración cuando el valor es mayor que el número de macrobloques en el marco.<br/>                                                                                                                                                                         |
| 1                                       | Es un entero que indica el tamaño de cada sector del marco en unidades de bits. <br/> El codificador debe iniciar un nuevo segmento en el adaptativo macrobloque que hace que el número de bits del segmento supere este valor (por lo que el tamaño de cada segmento siempre será menor o igual que este valor). Esto significa que el tamaño del último segmento podría ser significativamente menor que este valor. <br/> |
| 2                                       | Es un entero que indica el tamaño de cada sector del marco en unidades de filas de adaptativo macrobloque. <br/> El codificador debe rechazar la configuración cuando el valor es mayor que el número de filas de adaptativo macrobloque en el marco.<br/>                                                                                                                                                                 |



 

Si la aplicación no establece un valor para [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), el codificador debe devolver un error.

El valor predeterminado recomendado es tener un solo segmento para todo el marco.

Algunos codificadores pueden codificar segmentos en paralelo y, por tanto, el rendimiento podría verse afectado en función de la configuración del control del segmento. Por ejemplo, la codificación de un fotograma como un solo segmento podría ser más lenta que si el marco se codificara como varios segmentos.

La configuración del control de segmento es dinámica y se puede cambiar durante la sesión de codificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




