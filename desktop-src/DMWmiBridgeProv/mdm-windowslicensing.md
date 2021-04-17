---
title: MDM_WindowsLicensing (clase)
description: La \_ clase WindowsLicensing de MDM está diseñada para escenarios de administración relacionados con licencias.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing (clase)
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
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656521"
---
# <a name="mdm_windowslicensing-class"></a>\_Clase WindowsLicensing de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

La **clase \_ WindowsLicensing de MDM** está diseñada para escenarios de administración relacionados con licencias. Actualmente, el ámbito se limita a las actualizaciones de edición de dispositivos móviles y de escritorio de Windows 10, como Windows 10 Pro a Windows 10 Enterprise. Además, este CSP proporciona la capacidad de activar o cambiar la clave de producto de los dispositivos de escritorio de Windows 10.

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

La **clase \_ WindowsLicensing de MDM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ WindowsLicensing de MDM** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></td>
<td style="text-align: left;">Instala una clave de producto para dispositivos de escritorio de Windows 10. No se reinicia.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></td>
<td style="text-align: left;">Método para comprobar si se puede usar la clave de producto especificada para una actualización de edición, activación o cambio de una clave de producto de Windows 10 para dispositivos de escritorio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></td>
<td style="text-align: left;">Proporcione una licencia para una actualización de edición de dispositivos Windows 10 Mobile.<br/>
<blockquote>
[!Note]<br />
Este proceso de actualización no requiere un reinicio del sistema.
</blockquote>
<br/> <br/> El tipo de fecha es XML.<br/> La operación admitida es Execute.<br/>
<blockquote>
[!Important]<br />
El contenido del archivo de licencia XML debe tener un carácter de escape correcto (es decir, no debe ser simplemente un XML copiado), de lo contrario se producirá un error en la actualización de edición en dispositivos Windows 10 Mobile. Para obtener más información sobre el escape correcto del archivo de licencia XML, vea la sección 2,4 de la <a href="https://www.w3.org/TR/xml/">especificación XML del consorcio W3C</a>. El archivo de licencia XML se adquiere del centro de servicios de licencias por volumen de Microsoft. Su organización debe tener un contrato de licencias por volumen con Microsoft para tener acceso al portal.
</blockquote>
<br/> A continuación se indican las rutas de actualización de la edición válidas al usar este nodo a través de un paquete MDM o de aprovisionamiento:
<ul>
<li>Windows 10 Mobile para Windows 10 Mobile Enterprise<br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></td>
<td style="text-align: left;">Desencadena que el dispositivo tome la clave de producto y actualice la edición del cliente.
<blockquote>
[!Note]<br />
Este proceso de actualización requiere un reinicio del sistema.
</blockquote>
<br/> <br/> La operación admitida es Execute.<br/> Cuando se inserta una clave de producto de un servidor MDM en el dispositivo de un usuario, <strong>changepk.exe</strong> se ejecuta con la clave de producto. Una vez que se completa, se muestra una notificación al usuario que indica que hay disponible una nueva edición de Windows 10. Después, el usuario puede reiniciar el sistema manualmente o, después de dos horas, el dispositivo se reiniciará automáticamente para completar la actualización. El usuario recibirá una notificación de recordatorio 10 minutos antes del reinicio automático.<br/> Una vez que se reinicia el dispositivo, se completa el proceso de actualización de la edición. El usuario recibirá una notificación de la actualización correcta.
<blockquote>
[!Important]<br />
Si otra directiva requiere que se reinicie el sistema cuando se está ejecutando <strong>changepk.exe</strong> , se producirá un error en la actualización de la edición.
</blockquote>
<br/> <br/> Si se especifica una clave de producto en un paquete de aprovisionamiento y el usuario inicia la instalación del paquete, se muestra una notificación al usuario que indica que el sistema se reiniciará para completar la instalación del paquete. Tras el consentimiento explícito del usuario para continuar, el paquete continúa la instalación y <strong>changepk.exe</strong> se ejecuta con la clave de producto. El usuario recibirá una notificación de recordatorio de 30 segundos antes del reinicio automático. <br/> Una vez que se reinicia el dispositivo, se completa el proceso de actualización de la edición. El usuario recibirá una notificación de la actualización correcta. <br/> Este nodo también se puede usar para activar o cambiar una clave de producto en una edición determinada del dispositivo de escritorio de Windows 10 mediante la especificación de una clave de producto. La activación o el cambio de una clave de producto no requiere un reinicio y es un proceso silencioso para el usuario.<br/>
<blockquote>
[!Important]<br />
La clave de producto especificada debe tener 29 caracteres (es decir, debe incluir guiones); de lo contrario, se producirá un error en la activación, la actualización de edición o el cambio de clave de producto en los dispositivos de escritorio de Windows 10. La clave de producto se adquiere del centro de servicios de licencias por volumen de Microsoft. Su organización debe tener un contrato de licencias por volumen con Microsoft para tener acceso al portal.
</blockquote>
<br/> A continuación se indican las rutas de actualización de edición válidas al usar este nodo a través de un MDM:
<ul>
<li>Educación de Windows 10 Enterprise a Windows 10</li>
<li>Windows 10 Home a Windows 10 Education</li>
<li>Windows 10 Pro a Windows 10 Education</li>
<li>Windows 10 Pro a Windows 10 Enterprise</li>
</ul>
<br/> La activación o el cambio de una clave de producto se puede llevar a cabo en las siguientes ediciones:
<ul>
<li>Windows 10 Education</li>
<li>Windows 10 Enterprise</li>
<li>Windows 10 Home</li>
<li>Windows 10 Pro</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

La **clase \_ WindowsLicensing de MDM** tiene estas propiedades.

<dl> <dt>

[Edición](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
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

Identifica el nombre del nodo primario.

</dd> <dt>

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/".

</dd> <dt>

[Estado](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | DMMap de MDM raíz de \\ CIMv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

