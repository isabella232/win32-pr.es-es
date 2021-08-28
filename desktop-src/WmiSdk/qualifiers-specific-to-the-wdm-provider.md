---
description: El proveedor de WDM usa los siguientes calificadores en los archivos MOF del controlador de dispositivo cuando extraen datos de WNODE para generar instancias de clases de controladores WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Calificadores específicos del proveedor de WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 673b53d8cea23cd044175129af85c367f6f20c8dc92240c8bdf52f34708d96f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996085"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Calificadores específicos del proveedor de WDM

El proveedor de [WDM](/windows/desktop/WmiCoreProv/wdm-provider) usa los siguientes calificadores en los archivos MOF del controlador de dispositivo cuando extraen datos de WNODE para generar instancias de clases de controladores WDM.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

Tipo de datos: **DWORD, array, uint8, uint16, uint32, sint8, sint16 o sint32.**

Se aplica a: propiedades

Un valor que falta para esta propiedad debe representarse mediante **NULL** en lugar de 0 (cero).

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Tipo de datos: **uint32**

Se aplica a: propiedades

Índice en el WNODE de los datos de la propiedad. El proveedor WDM usa este calificador para determinar cómo se formatearán los datos al extraer datos del WNODE y generar clases WMI. El valor inicial es 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Tipo de datos: **uint32**

Se aplica a: clases

Indicación del costo de recursos para acceder al bloque de datos. Por ejemplo, la información de geometría de disco no requiere que se obtengan muchos recursos porque está disponible en la extensión del dispositivo. El rendimiento de lectura y escritura en disco consume más recursos porque requiere trabajo adicional en cada operación de lectura y escritura. Por lo tanto, el valor del calificador **WMIExpense** es mayor para el rendimiento de lectura y escritura del disco.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Tipo de datos: **uint32**

Se aplica a: métodos

Índice en el WNODE de los datos de la propiedad. El proveedor WDM usa este calificador para determinar cómo se formatearán los datos al extraer datos del WNODE y generar clases WMI. El valor inicial es 1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

