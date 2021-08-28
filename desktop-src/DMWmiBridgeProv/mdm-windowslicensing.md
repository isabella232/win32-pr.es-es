---
title: MDM_WindowsLicensing clase
description: La clase MDM \_ WindowsLicensing está diseñada para escenarios de administración relacionados con licencias.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing clase
- MDM_WindowsLicensing clase, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9470b72cb6a50323af9294be4a6506682fc7aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480931"
---
# <a name="mdm_windowslicensing-class"></a>Mdm \_ WindowsLicensing (clase)

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ WindowsLicensing** está diseñada para escenarios de administración relacionados con licencias. Actualmente, el ámbito se limita a las actualizaciones de edición Windows 10 dispositivos móviles y de escritorio, como Windows 10 Pro a Windows 10 Enterprise. Además, este CSP proporciona la capacidad de activar o cambiar la clave de producto de Windows 10 dispositivos de escritorio.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a>Miembros

La **clase \_ Mdm WindowsLicensing** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ Mdm WindowsLicensing** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a> | Instala una clave de producto para Windows 10 dispositivos de escritorio. No se reinicia.<br /> | 
| <a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a> | Método para comprobar si la clave de producto especificada se puede usar para una actualización de edición, activación o cambio de una clave de producto de Windows 10 dispositivos de escritorio.<br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a> | Proporcione una licencia para una actualización de edición de Windows 10 dispositivos móviles.<br /><blockquote>[!Note]<br />Este proceso de actualización no requiere un reinicio del sistema.</blockquote><br /><br /> El tipo de fecha es XML.<br /> La operación admitida es Execute.<br /><blockquote>[!Important]<br />El contenido del archivo de licencia XML debe tener una secuencia de escape correcta (es decir, no debe ser simplemente un XML copiado), de lo contrario, se producirá un error en la actualización de la edición en Windows 10 dispositivos móviles. Para obtener más información sobre el escape adecuado del archivo de licencia XML, vea la sección 2.4 de la especificación <a href="https://www.w3.org/TR/xml/">XML de W3C.</a> El archivo de licencia XML se adquiere del Centro de servicios de licencias por volumen de Microsoft. Su organización debe tener un contrato de licencias por volumen con Microsoft para acceder al portal.</blockquote><br /> Las siguientes son rutas de actualización de edición válidas cuando se usa este nodo a través de un paquete mdm o de aprovisionamiento:<ul><li>Windows 10 Mobileto Windows 10 Mobile Enterprise<br /></li></ul><br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a> | Desencadena el dispositivo para tomar la clave de producto y actualizar la edición del cliente.<blockquote>[!Note]<br />Este proceso de actualización requiere un reinicio del sistema.</blockquote><br /><br /> La operación admitida es Execute.<br /> Cuando se inserta una clave de producto desde un servidor MDM al dispositivo de un <strong> usuario, </strong>changepk.exeejecuta con la clave de producto. Una vez completada, se muestra una notificación al usuario de que hay disponible una nueva Windows 10 de datos. A continuación, el usuario puede reiniciar el sistema manualmente o, después de dos horas, el dispositivo se reiniciará automáticamente para completar la actualización. El usuario recibirá una notificación de recordatorio 10 minutos antes del reinicio automático.<br /> Una vez reiniciado el dispositivo, se completa el proceso de actualización de edición. El usuario recibirá una notificación de la actualización correcta.<blockquote>[!Important]<br />Si otra directiva requiere un reinicio del sistema que se produce <strong>changepk.exe</strong> se está ejecutando, se producirá un error en la actualización de la edición.</blockquote><br /><br /> Si se introduce una clave de producto en un paquete de aprovisionamiento y el usuario comienza la instalación del paquete, se muestra una notificación al usuario de que su sistema se reiniciará para completar la instalación del paquete. Tras el consentimiento explícito del usuario para continuar, el paquete continúa la instalación <strong> ychangepk.exe</strong> ejecuta con la clave de producto. El usuario recibirá una notificación de recordatorio 30 segundos antes del reinicio automático. <br /> Una vez reiniciado el dispositivo, se completa el proceso de actualización de edición. El usuario recibirá una notificación de la actualización correcta. <br /> Este nodo también se puede usar para activar o cambiar una clave de producto en una edición determinada de Windows 10 de escritorio especificando una clave de producto. La activación o el cambio de una clave de producto no requiere un reinicio y es un proceso silencioso para el usuario.<br /><blockquote>[!Important]<br />La clave de producto especificada debe tener 29 caracteres (es decir, debe incluir guiones), de lo contrario, se producirá un error en la activación, actualización de edición o cambio de clave de producto en Windows 10 dispositivos de escritorio. La clave de producto se adquiere en el Centro de servicios de licencias por volumen de Microsoft. Su organización debe tener un contrato de licencias por volumen con Microsoft para acceder al portal.</blockquote><br /> Las siguientes son rutas de actualización de edición válidas cuando se usa este nodo a través de una MDM:<ul><li>Windows 10 Enterprise a Windows 10 Education</li><li>Windows 10 Home a Windows 10 Education</li><li>Windows 10 Pro a Windows 10 Education</li><li>Windows 10 Pro a Windows 10 Enterprise</li></ul><br /> La activación o el cambio de una clave de producto se pueden llevar a cabo en las siguientes ediciones:<ul><li>Windows 10 Education</li><li>Windows 10 Enterprise</li><li>Windows 10 Home</li><li>Windows 10 Pro</li></ul><br /> | 




 

### <a name="properties"></a>Propiedades

La **clase \_ Mdm WindowsLicensing** tiene estas propiedades.

<dl> <dt>

[Edición](/windows/client-management/mdm/windowslicensing-csp#edition)
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

Identifica el nombre del nodo primario.

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
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

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/"

</dd> <dt>

[Estado](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
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
| Espacio de nombres<br/>                | DMMap \\ de MDM \\ de CIMv2 \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

