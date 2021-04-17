---
description: El proveedor de WDM usa los siguientes calificadores en archivos MOF de controlador de dispositivo cuando extraen datos de WNODEs para generar instancias de clases de controlador WDM.
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
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696668"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Calificadores específicos del proveedor de WDM

El [proveedor de WDM](/windows/desktop/WmiCoreProv/wdm-provider) usa los siguientes calificadores en archivos MOF de controlador de dispositivo cuando extraen datos de WNODEs para generar instancias de clases de controlador WDM.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

Tipo de datos: **DWORD, array, Uint8, UInt16, UInt32, sint8, sint16 o sint32.**

Se aplica a: propiedades

Un valor que falta para esta propiedad debe estar representado por **null** en lugar de 0 (cero).

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Tipo de datos: **UInt32**

Se aplica a: propiedades

Índice en el WNODE de los datos para la propiedad. El proveedor WDM utiliza este calificador para determinar cómo se da formato a los datos al extraer datos de WNODE y generar clases WMI. El valor inicial es 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Tipo de datos: **UInt32**

Se aplica a: clases

Indicación del costo de recursos para tener acceso al bloque de datos. Por ejemplo, la información de geometría de disco no requiere una gran cantidad de recursos para obtener porque está disponible en la extensión de dispositivo. El rendimiento de lectura y escritura de disco es más intensivo porque requiere trabajo adicional en cada operación de lectura/escritura. Por lo tanto, el valor de calificador **WMIExpense** es mayor para el rendimiento de lectura y escritura de disco.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Tipo de datos: **UInt32**

Se aplica a: métodos

Índice en el WNODE de los datos para la propiedad. El proveedor WDM utiliza este calificador para determinar cómo se da formato a los datos al extraer datos de WNODE y generar clases WMI. El valor inicial es 1.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

