---
title: MDM_DevDetail_Microsoft02 clase
description: La clase MDM DevDetail Microsoft02 controla el objeto de administración que proporciona parámetros específicos del dispositivo \_ \_ al servidor OMA DM.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- MDM_DevDetail_Microsoft02 clase
- MDM_DevDetail_Microsoft02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc995d04452a49bfb6420d4b7e8424ab06b7f4023440568f841564fef532aa2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053605"
---
# <a name="mdm_devdetail_microsoft02-class"></a>Mdm \_ DevDetail \_ Microsoft02 (clase)

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ DevDetail \_ Microsoft02** controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM. Estos parámetros de dispositivo no se envían desde el cliente al servidor automáticamente, pero los servidores pueden consultar estos parámetros mediante comandos de OMA DM.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a>Miembros

La **clase MDM \_ DevDetail \_ Microsoft02** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MDM \_ DevDetail \_ Microsoft02** tiene estas propiedades.

<dl> <dt>

[CommercializationOperator](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[DeviceName](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
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

Identifica el nombre del nodo primario. Para esta clase, la cadena es "Microsoft".

</dd> <dt>

[LocalTime](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[MobileID](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[OSPlatform](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./DevDetail/Ext".

</dd> <dt>

[ProcessorArchitecture](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[ProcessorType](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[RadioSwV](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Devuelve el número de versión de software de la pila de radio.

</dd> <dt>

[Resolución](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

