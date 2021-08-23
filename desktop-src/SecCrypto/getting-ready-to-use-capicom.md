---
description: Las aplicaciones que usan objetos CAPICOM deben crearse mediante CAPICOM.dll. CAPICOM.dll estar presente y registrado en tiempo de ejecución para usar objetos CAPICOM.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Prepararse para usar CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a6b76c293395fd0979cf5c304b27bae75622996279bd891b8c0c1301dca82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006642"
---
# <a name="getting-ready-to-use-capicom"></a>Prepararse para usar CAPICOM

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Las aplicaciones que usan objetos CAPICOM deben crearse mediante CAPICOM.dll. CAPICOM.dll estar presente y registrado en tiempo de ejecución para usar objetos CAPICOM. CAPICOM.dll agregar a las referencias Visual Basic proyectos para usar objetos CAPICOM.

CAPICOM está disponible como un archivo redistribuible que se puede descargar de [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281). Para obtener información sobre las versiones de CAPICOM, [vea Versiones de CAPICOM](capicom-versions.md).

**Para registrar CAPICOM.dll**

-   En un símbolo del sistema, cambie el directorio al directorio donde CAPICOM.dll almacenamiento y, a continuación, escriba el siguiente comando:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Limitaciones de código de ejemplo

Para proporcionar código más conciso y legible, los principios de una buena práctica de programación no siempre se siguen en estos ejemplos. En concreto, solo se muestran respuestas de error limitadas. Las aplicaciones de trabajo siempre deben comprobar los códigos de error devueltos y realizar las acciones adecuadas cuando se encuentra un error.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Contenedores de claves, claves y certificados necesarios en CAPICOM

Aunque cualquier usuario puede realizar algunas operaciones con objetos CAPICOM en cualquier equipo, la creación de firmas digitales y la recuperación del contenido de texto no cifrado de un mensaje con sobres mediante objetos CAPICOM son operaciones [*basadas*](../secgloss/d-gly.md) en certificados. El usuario que crea una firma digital y el usuario que recupera el contenido cifrado de un mensaje con sobre deben tener un certificado digital con una clave privada asociada disponible. Si no hay un certificado con una clave privada asociada, se producirá un error en la operación criptográfica. Los usuarios de aplicaciones CAPICOM deben asegurarse de que tienen el certificado adecuado y la clave privada disponible cuando se ejecutan las aplicaciones.

Algunos ejemplos de las secciones siguientes realizan [](../secgloss/p-gly.md) operaciones que requieren un par de claves pública y privada disponible para cifrar y descifrar archivos, mensajes y firmas. Muchos de estos programas se compilarán y ejecutarán, pero se producirá un error en tiempo de ejecución sin la existencia de contenedores de [*claves,*](../secgloss/k-gly.md)claves, almacenes de certificados y certificados [*adecuados*](../secgloss/c-gly.md) en esos almacenes.

**Para crear un certificado autofirmado**

1.  Instale las herramientas de firma. Se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows, el Kit de desarrollo de software de plataforma (SDK) o .NET Framework SDK.
2.  Después Makecert.exe descarga, ejecute el siguiente comando en un símbolo del sistema, sustituyendo un nombre de usuario por *UserName,* un nombre de organización para *OrganizationName* y un nombre de empresa para *CompanyName*:

    **makecert -r -n "cn=**_UserName_*_, ou=_*_OrganizationName_*_, o=_*_CompanyName_*_" -ss my_*

3.  El certificado se puede colocar en el almacén Mi del usuario actual. Importe el certificado creado en el almacén raíz para que sea de confianza.

 

 
