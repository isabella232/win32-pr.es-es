---
title: MDM_PassportForWork_Remote03 (clase)
description: La \_ clase Remote03 de MDM PassportForWork \_ define la configuración de la Directiva remota de Windows Hello para empresas.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- MDM_PassportForWork_Remote03 (clase)
- MDM_PassportForWork_Remote03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079188"
---
# <a name="mdm_passportforwork_remote03-class"></a>\_Clase Remote03 PassportForWork de MDM \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ \_ Remote03 de MDM PassportForWork** define la configuración de la Directiva remota de Windows Hello para empresas.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ Remote03 de MDM PassportForWork** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Remote03 de MDM PassportForWork** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo interior para definir directivas de Windows Hello para empresas remotas. Este nodo se agregó en Windows 10, versión 1511.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo para definir la configuración de la Directiva de Windows Hello para empresas.

</dd> <dt>

[UseRemotePassport](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

