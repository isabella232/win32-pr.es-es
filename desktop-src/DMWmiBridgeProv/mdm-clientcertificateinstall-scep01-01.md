---
title: MDM_ClientCertificateInstall_SCEP01_01 clase
description: La clase MDM \_ ClientCertificateInstall \_ SCEP01 01 permite el acceso al nodo para la instalación de certificados SCEP, mediante identificadores únicos para diferenciar las distintas solicitudes de instalación \_ de certificados.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- MDM_ClientCertificateInstall_SCEP01_01 clase
- MDM_ClientCertificateInstall_SCEP01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152b5867a6b93f00a0389148f72a5280ae8de1616e8338dad1a36841195cb67a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077329"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a>Clase \_ MDM ClientCertificateInstall \_ SCEP01 \_ 01

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** permite el acceso al nodo para la instalación de certificados SCEP, mediante identificadores únicos para diferenciar diferentes solicitudes de instalación de certificados.

Necesario para la instalación de certificados SCEP.

Las operaciones admitidas son Get, Add y Delete.

Al llamar a Delete en este nodo, se debe eliminar el certificado SCEP correspondiente.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a>Miembros

La **clase \_ MDM ClientCertificateInstall \_ SCEP01 \_ 01** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MDM \_ ClientCertificateInstall \_ SCEP01 \_ 01** tiene estas propiedades.

<dl> <dt>

[CertThumbprint](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[ErrorCode](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
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

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, un identificador único para diferenciar las distintas solicitudes de instalación de certificados.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario.

La cadena es "./Vendor/MSFT/ClientCertificateInstall/SCEP"

</dd> <dt>

[RespondentServerUrl](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

[Estado](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

