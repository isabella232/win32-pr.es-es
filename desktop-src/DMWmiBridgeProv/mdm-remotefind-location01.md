---
title: MDM_RemoteFind_Location01 clase
description: La clase \_ MDM RemoteFind \_ Location01 recupera la información de ubicación de un dispositivo determinado.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- MDM_RemoteFind_Location01 clase
- MDM_RemoteFind_Location01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36942badfe975a28d5212e502ab28984fa745f4a7563c39ed1cebb7d1b5dbcef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077029"
---
# <a name="mdm_remotefind_location01-class"></a>Clase \_ RemoteFind \_ Location01 de MDM

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase \_ MDM RemoteFind \_ Location01** recupera la información de ubicación de un dispositivo determinado.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a>Miembros

La **clase \_ Mdm RemoteFind \_ Location01** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ MDM RemoteFind \_ Location01** tiene estas propiedades.

<dl> <dt>

[Precisión](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[Age](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[Altitud](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[AltitudAcencia](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es "Location".

</dd> <dt>

[Latitud](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[Longitud](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/RemoteFind"

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                       |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

