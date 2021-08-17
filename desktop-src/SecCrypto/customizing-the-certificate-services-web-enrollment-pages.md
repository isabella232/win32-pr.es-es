---
description: Servicios de certificados proporciona páginas de inscripción web que se pueden usar para solicitar certificados.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Personalización de páginas de inscripción web de Servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0132ce4e5e1fef588ffc429597717433dd1b780d2f7f35f9c886f1978b5b318a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767800"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Personalización de páginas de inscripción web de Servicios de certificados

[*Servicios de certificados*](../secgloss/c-gly.md) proporciona páginas de inscripción web que se pueden usar para solicitar certificados. Un administrador puede personalizar algunos de los elementos que se pueden ver en las páginas de inscripción web. sin embargo, debe estar familiarizado con las páginas de inscripción web y el scripting web antes de realizar cambios. Para obtener más información sobre el scripting web, vea [Scripting](/previous-versions/ms950396(v=msdn.10)).

Los valores predeterminados de los campos Nombre distintivo para Organización, Unidad organizativa, Localidad, Estado [](../secgloss/c-gly.md) y País o Región son los valores especificados para la entidad de certificación (CA) cuando se instala Certificate Services. Estos valores predeterminados aparecen en las páginas web y el usuario puede cambiarlo durante el proceso de inscripción de certificados. Sin embargo, si desea que aparezcan otros valores predeterminados en las páginas web, puede editar el archivo Certdat.inc (en la ruta de acceso \\ *WindowsDirectory* \\ System32 \\ Certsrv ); en concreto, puede asignar valores personalizados a las siguientes variables proporcionadas para la \\ personalización.



| Variable            | Descripción                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Empresa predeterminada (aparece en la [*solicitud de certificado*](../secgloss/c-gly.md) como el campo Organización [*X.509).*](../secgloss/x-gly.md) |
| sDefaultOrgUnit     | Departamento predeterminado (aparece en la solicitud de certificado como el campo Unidad organizativa X.509).                                                                                                                                           |
| sDefaultLocality    | Ciudad predeterminada (aparece en la solicitud de certificado como el campo Ubicación X.509).                                                                                                                                                            |
| sDefaultState       | Estado o provincia predeterminados (aparece en la solicitud de certificado como el campo Estado X.509).                                                                                                                                                     |
| sDefaultCountry     | País o región predeterminado (aparece en la solicitud de certificado como el campo País o región X.509).                                                                                                                                            |
| nPendingTimeoutDays | Número de días en los que el usuario puede recuperar un certificado pendiente una vez solicitado.                                                                                                                                          |



 

No se debe cambiar ninguna otra variable en el archivo Certdat.inc.

En el ejemplo siguiente se establece la unidad organizativa predeterminada en "Marketing".


```VB
sDefaultOrgUnit="Marketing"
```



Además, puede editar el archivo Certrqtp.inc para agregar, cambiar o quitar plantillas de certificado o tipos disponibles para el usuario. [](../secgloss/c-gly.md) Estas plantillas y tipos, así como la información relacionada, se encuentran en una matriz dimensionada denominada rgAvailReqTypes(*m*,5).

Esta matriz, como todas las matrices de Visual Basic Scripting Edition, está basada en cero y, como resultado, la primera dimensión de la matriz, *m*, asigna memoria para los elementos *m*+1. Por lo tanto, si al personalizar las páginas web, debe modificar el número de elementos de la matriz rgAvailReqTypes, establezca la dimensión *m* en uno menos que el número total de elementos que necesita. Por ejemplo, si va a tener siete plantillas de certificado, cambie la declaración de rgAvailReqTypes como se muestra en el ejemplo siguiente.


```VB
Dim rgAvailReqTypes(6,5)
```



La segunda dimensión de la matriz, que siempre tiene el valor cinco, asigna los seis campos que componen cada elemento. Estos seis campos representan la plantilla o el tipo de certificado, el nombre para mostrar asociado a esta plantilla o tipo, y si la plantilla requiere extensiones [*seguras*](../secgloss/s-gly.md) o multipropósito de Correo electrónico de Internet (S/MIME).

Para que sea más fácil comprender a cuál de estos campos se accede, Certrqtp.inc también proporciona las siguientes constantes que puede usar al establecer valores de campo.



| Constante                              | Descripción                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FIELD \_ OID**                        | (Se aplica a las CA independientes) Indexe al primer campo del elemento; representa un [*identificador de objeto*](../secgloss/o-gly.md) (OID) para un tipo de certificado.<br/>                                                                                                           |
| **PLANTILLA DE \_ CAMPO**                   | (Se aplica a las CA empresariales) Indexe al primer campo del elemento; representa una plantilla de certificado.<br/>                                                                                                                                                                                                                           |
| **FIELD \_ FRIENDLYNAME**               | Indexe al segundo campo del elemento; representa el nombre para mostrar (que el usuario verá al inscribirse) del elemento en el primer campo.                                                                                                                                                                                               |
| **FIELD \_ CSPLIST**                    | Indexe al tercer campo del elemento. Lista de nombres [*de proveedor de servicios criptográficos*](../secgloss/c-gly.md) permitidos por la plantilla. Cada nombre de la lista está separado por un signo de interrogación (?).                                                    |
| **FIELD \_ CSPLIST2**                   | Indexe al cuarto campo del elemento. Lista secundaria de nombres [*de proveedor de servicios criptográficos*](../secgloss/c-gly.md) permitidos por la plantilla. Cada nombre de la lista está separado por un signo de interrogación (?). Esta lista proporciona un valor predeterminado diferente. |
| **CAMPO \_ EXPORTABLE**                 | Indexe al quinto campo del elemento. Indica si la plantilla especifica que la clave debe ser exportable. Si este campo contiene "True", la clave es exportable. Si este campo contiene "False", la clave no se puede exportar.                                                                                                        |
| **EL CAMPO \_ NECESITA \_ FUNCIONALIDADES DE \_ SMIME** | Esta constante no se admite.                                                                                                                                                                                                                                                                                                      |



 

Por ejemplo, las expresiones siguientes asignan el OID de 1.3.6.1.5.5.7.3.2 al primer campo del primer elemento y asignan "Certificado de explorador web" al segundo campo del primer elemento (el valor de matriz de cero indexa el primer elemento).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



El resultado de estas asignaciones es que el usuario verá el texto Certificado de explorador **web** al inscribirse y, si el usuario selecciona Certificado de explorador **web**, la solicitud de certificado contendrá el OID 1.3.6.1.5.5.7.3.2. [](../secgloss/c-gly.md)

El archivo Certrqtp.inc también contiene constantes que se usan para los nombres para mostrar de los tipos o plantillas de certificado. En el ejemplo siguiente se muestra el formato .


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Estas constantes se definen en un bloque del archivo Certrqtp.inc y esta agrupación facilita la asignación de un valor personalizado a cada una de ellas. Esto resulta especialmente útil cuando se localizan los nombres para mostrar de las versiones internacionales de las páginas web.

Por último, el archivo Certrqtp.inc contiene una variable que representa el número de plantillas o tipos de certificado en la matriz rgAvailReqTypes. A diferencia de la *dimensión m* de la matriz, establezca el valor de la variable nAvailReqTypes en el número real de plantillas o tipos de certificado que usará la instalación; este valor no debe ser mayor que *m*+1. Aunque se declara cerca de la parte superior del archivo Certrqtp.inc, a nAvailReqTypes se le asigna un valor una vez rellenada la matriz rgAvailReqTypes, lo que facilita ver cuántos elementos usa realmente la matriz. El valor nAvailReqTypes se usa en una iteración en otra parte de las páginas de inscripción web, por lo que es importante que esta variable refleje con precisión el número de plantillas o tipos de certificado que desea que el usuario pueda ver.

Tenga en cuenta [](../secgloss/c-gly.md) que simplemente agregar plantillas de certificado y tipos al archivo Certrqtp.inc no garantiza que el usuario pueda obtener un certificado con esos rasgos; La entidad de certificación debe estar autorizada para emitir un certificado para el tipo o plantilla de certificado especificado.

Las instalaciones pueden crear sus propias aplicaciones o páginas web para solicitar y recibir un certificado. Los [**objetos ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) [**e ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) permiten a los programadores o scriptadores compilar [*aplicaciones de solicitud de*](../secgloss/c-gly.md) certificado.

Para solicitar que se emita un certificado en una [*tarjeta inteligente,*](../secgloss/s-gly.md)puede usar el Control de inscripción de tarjetas inteligentes. Para obtener más información y código de ejemplo, [**vea ISCrdEnr**](iscrdenr.md).

 

 
