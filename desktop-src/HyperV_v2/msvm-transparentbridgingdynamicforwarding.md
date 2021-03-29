---
description: Conecta un servicio de puente transparente a una entrada de reenvío dinámica (dirección MAC aprendida).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Msvm_TransparentBridgingDynamicForwarding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001400"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a>MSVM \_ TransparentBridgingDynamicForwarding (clase)

Conecta un servicio de puente transparente a una entrada de reenvío dinámica (dirección MAC aprendida).

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ TransparentBridgingDynamicForwarding** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ TransparentBridgingDynamicForwarding** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa el servicio de puente transparente.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) que representa la entrada de reenvío dinámico de la base de datos de reenvío.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ TransparentBridgingDynamicForwarding** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[**\_TRANSPARENTBRIDGINGDYNAMICFORWARDING CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

