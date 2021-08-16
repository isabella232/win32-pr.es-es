---
title: MDM_EnterpriseDataProtection_Settings01 clase
description: La clase MDM EnterpriseDataProtection Settings01 se usa para configurar Windows Information Protection \_ \_ (WIP) (anteriormente conocido como Enterprise Data Protection).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- MDM_EnterpriseDataProtection_Settings01 clase
- MDM_EnterpriseDataProtection_Settings01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e80502ff724a43f1034922b0734fe128124c193f0ef5319ee2976257d26fbe3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165838"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a>Clase MDM \_ EnterpriseDataProtection \_ Settings01

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ EnterpriseDataProtection \_ Settings01** se usa para configurar Windows Information Protection (WIP) (anteriormente conocido como Enterprise Data Protection). Para más información sobre WIP, consulte Protección de los datos empresariales mediante la protección de datos [empresariales (EDP).](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a>Miembros

La **clase MDM \_ EnterpriseDataProtection \_ Settings01** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MDM \_ EnterpriseDataProtection \_ Settings01** tiene estas propiedades.

<dl> <dt>

[AllowAzureRMSForEDP](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[AllowUserDecryption](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[DataRecoveryCertificate](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **Octetstring**
</dt> </dl>

</dd> <dt>

[EDPEnforcementLevel](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[EDPShowIcons](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[EnterpriseProtectedDomainNames](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
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

Identifica el nombre del nodo primario. Para esta clase, la cadena es "Configuración".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseDataProtection"

</dd> <dt>

[RevokeOnUnenroll](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[RMSTemplateIDForEDP](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[SMBAutoEncryptedFileExtensions](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 

