---
description: Servicios de Certificate Server proporciona páginas de inscripción Web que se pueden usar para solicitar certificados.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Personalización de las páginas de inscripción Web de servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb2fbf421eceb1ebf0b15379aca5d0788a992ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913046"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Personalización de las páginas de inscripción Web de servicios de certificados

[*Servicios de Certificate Server*](../secgloss/c-gly.md) proporciona páginas de inscripción Web que se pueden usar para solicitar certificados. Un administrador puede personalizar algunos de los elementos que se pueden ver en las páginas de inscripción Web. sin embargo, debe estar familiarizado con las páginas de inscripción Web y el scripting Web antes de realizar cambios. Para obtener más información sobre el scripting Web, vea [scripting](/previous-versions/ms950396(v=msdn.10)).

Los valores predeterminados para los campos de nombre distintivo de organización, unidad organizativa, localidad, estado y país o región son los valores especificados para la [*entidad de certificación*](../secgloss/c-gly.md) (CA) cuando se instala servicios de Certificate Server. Estos valores predeterminados aparecen en las páginas web y el usuario puede cambiarlos durante el proceso de inscripción de certificados. Sin embargo, si desea que aparezcan otros valores predeterminados en las páginas web, puede editar el archivo certdat. Inc (en la ruta de acceso \\ *WindowsDirectory* \\ system32 \\ CertSrv \\ ); en concreto, puede asignar valores personalizados a las siguientes variables proporcionadas para la personalización.



| Variable            | Descripción                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Empresa predeterminada (aparece en la [*solicitud de certificado*](../secgloss/c-gly.md) como el campo organización [*X. 509*](../secgloss/x-gly.md) ). |
| sDefaultOrgUnit     | Departamento predeterminado (aparece en la solicitud de certificado como el campo de unidad organizativa X. 509).                                                                                                                                           |
| sDefaultLocality    | Ciudad predeterminada (aparece en la solicitud de certificado como el campo de ubicación X. 509).                                                                                                                                                            |
| sDefaultState       | Estado o provincia predeterminados (aparece en la solicitud de certificado como el campo de estado X. 509).                                                                                                                                                     |
| sDefaultCountry     | País o región predeterminados (aparece en la solicitud de certificado como el campo de país o región X. 509).                                                                                                                                            |
| nPendingTimeoutDays | Número de días en los que el usuario puede recuperar un certificado pendiente después de solicitarlo.                                                                                                                                          |



 

No se deben cambiar otras variables en el archivo certdat. Inc.

En el ejemplo siguiente se establece la unidad organizativa predeterminada en "Marketing".


```VB
sDefaultOrgUnit="Marketing"
```



Además, puede editar el archivo Certrqtp. Inc para agregar, cambiar o quitar plantillas de [*certificado*](../secgloss/c-gly.md) o tipos disponibles para el usuario. Estas plantillas y tipos, así como información relacionada, se encuentran en una matriz con dimensiones denominada rgAvailReqTypes (*m*, 5).

Esta matriz, como todas Visual Basic Scripting Edition matrices, está basada en cero y, como resultado, la primera dimensión de la matriz, *m*, asigna memoria para los elementos *m*+ 1. Por lo tanto, si en la personalización de las páginas web necesita modificar el número de elementos de la matriz rgAvailReqTypes, establezca la dimensión *m* en uno menos que el número total de elementos que necesita. Por ejemplo, si va a tener siete plantillas de certificado, cambie la declaración de rgAvailReqTypes como se muestra en el ejemplo siguiente.


```VB
Dim rgAvailReqTypes(6,5)
```



La segunda dimensión de la matriz, que siempre tiene el valor cinco, asigna los seis campos que componen cada elemento. Estos seis campos representan la plantilla o el tipo de certificado, el nombre para mostrar asociado a esta plantilla o tipo y si la plantilla requiere [*extensiones seguras multipropósito de correo Internet*](../secgloss/s-gly.md) (S/MIME).

Para facilitar la comprensión de los campos a los que se tiene acceso, Certrqtp. Inc también proporciona las siguientes constantes que se pueden usar al establecer los valores de los campos.



| Constante                              | Descripción                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OID del campo \_**                        | (Se aplica a las CA independientes) Índice del primer campo del elemento; representa un [*identificador de objeto*](../secgloss/o-gly.md) (OID) para un tipo de certificado.<br/>                                                                                                           |
| **plantilla de campo \_**                   | (Se aplica a las CA de empresa) Índice del primer campo del elemento; representa una plantilla de certificado.<br/>                                                                                                                                                                                                                           |
| **CAMPO \_ FRIENDLYNAME**               | Índice del segundo campo del elemento; representa el nombre para mostrar (que el usuario verá al inscribirse) del elemento en el primer campo.                                                                                                                                                                                               |
| **CAMPO \_ CSPLIST**                    | Índice del tercer campo del elemento. Una lista de nombres de [*proveedores de servicios de cifrado*](../secgloss/c-gly.md) permitidos por la plantilla. Cada nombre de la lista está separado por un signo de interrogación (?).                                                    |
| **CAMPO \_ CSPLIST2**                   | Índice del cuarto campo del elemento. Lista secundaria de nombres de [*proveedores de servicios de cifrado*](../secgloss/c-gly.md) permitidos por la plantilla. Cada nombre de la lista está separado por un signo de interrogación (?). Esta lista proporciona un valor predeterminado diferente. |
| **CAMPO \_ EXportable**                 | Índice del quinto campo del elemento. Indica si la plantilla especifica que la clave debe ser exportable. Si este campo contiene "true", la clave es exportable. Si este campo contiene "false", la clave no se exportable.                                                                                                        |
| **el \_ campo \_ necesita \_ funcionalidades SMIME** | Esta constante no se admite.                                                                                                                                                                                                                                                                                                      |



 

Por ejemplo, las expresiones siguientes asignan el OID de 1.3.6.1.5.5.7.3.2 al primer campo del primer elemento y asignan "certificado de explorador Web" al segundo campo del primer elemento (el valor de matriz de cero indiza el primer elemento).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



El resultado de estas asignaciones es que el usuario verá el **certificado del explorador Web** de texto al inscribirse y, si el usuario selecciona el certificado del **explorador Web**, la [*solicitud de certificado*](../secgloss/c-gly.md) contendrá el OID 1.3.6.1.5.5.7.3.2.

El archivo Certrqtp. Inc también contiene constantes que se usan para mostrar los nombres de las plantillas de certificado o los tipos. En el siguiente ejemplo se muestra el formato.


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Estas constantes se definen en un bloque en el archivo Certrqtp. Inc y esta agrupación facilita la asignación de cada uno de ellos a un valor personalizado. Esto es especialmente útil cuando se localizan los nombres para mostrar de las versiones internacionales de las páginas Web.

Por último, el archivo Certrqtp. Inc contiene una variable que representa el número de plantillas de certificado o tipos de la matriz rgAvailReqTypes. A diferencia de la dimensión *m* de la matriz, establezca el valor de la variable nAvailReqTypes en el número real de plantillas de certificado o tipos que utilizará la instalación. Este valor no debe ser mayor que *m*+ 1. Aunque se declara cerca de la parte superior del archivo Certrqtp. Inc, se asigna un valor a nAvailReqTypes una vez que se rellena la matriz rgAvailReqTypes, lo que facilita la visualización del número de elementos que se usan realmente en la matriz. El valor nAvailReqTypes se usa en una iteración en otra parte de las páginas de inscripción Web, por lo que es importante que esta variable refleje con precisión el número de plantillas de certificado o los tipos que desea que sean visibles para el usuario.

Tenga en cuenta que, al agregar simplemente plantillas y tipos de [*certificado*](../secgloss/c-gly.md) al archivo Certrqtp. Inc, no se garantiza que el usuario pueda obtener un certificado con esos rasgos. la entidad de certificación debe estar autorizada para emitir un certificado para la plantilla de certificado especificada o el tipo.

Las instalaciones pueden crear sus propias aplicaciones o páginas web para solicitar y recibir un certificado. Los objetos [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) y [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) permiten a los programadores o generadores de scripts crear aplicaciones de [*solicitud de certificado*](../secgloss/c-gly.md) .

Para solicitar un certificado que se va a emitir en una [*tarjeta inteligente*](../secgloss/s-gly.md), puede usar el control de inscripción de tarjetas inteligentes. Para obtener más información y código de ejemplo, vea [**ISCrdEnr**](iscrdenr.md).

 

 
