---
description: Representa la configuración y los parámetros operativos para las \_ instancias de ManagedElement de CIM.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: CIM_SettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19c62496b7980c265ff20ae0b1cdb050e311e4c5e09fd981b49b562eed14596b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647336"
---
# <a name="cim_settingdata-class"></a>Cim \_ SettingData (clase)

Representa la configuración y los parámetros operativos para [**las instancias de \_ ManagedElement**](cim-managedelement.md) de CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Miembros

La **clase \_ SettingData** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SettingData** de CIM tiene estas propiedades.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nombre descriptivo de una instancia de esta clase. Además, el nombre descriptivo se puede usar como índice para una búsqueda o consulta. El nombre no tiene que ser único dentro de un espacio de nombres.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma única una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Para garantizar la unidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse con el siguiente patrón: *OrgID*:*LocalID*
>
> -   *OrgID* debe incluir un nombre único con derechos de autor, marca comercial o que sea propiedad de la entidad empresarial que define la propiedad **InstanceID** o ser un identificador registrado asignado por una autoridad global reconocida.
> -   *OrgID* no debe contener dos puntos. El primer signo de dos puntos **de InstanceID** debe estar entre *OrgID* y *LocalID.*
> -   La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar los distintos elementos subyacentes del mundo real.
> -   Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **instanceID** resultante no se vuelva a usar en ninguna propiedad **InstanceID** producida por este proveedor u otros proveedores para este espacio de nombres.
> -   Para las instancias definidas por DMTF, el patrón debe usarse con *orgID* establecido en "CIM".

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

