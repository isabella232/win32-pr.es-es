---
description: Las aplicaciones que usan objetos CAPICOM deben crearse mediante CAPICOM.dll. CAPICOM.dll también debe estar presente y registrado en tiempo de ejecución para usar CAPICOM Objects.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Preparación para usar CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668224"
---
# <a name="getting-ready-to-use-capicom"></a>Preparación para usar CAPICOM

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

Las aplicaciones que usan objetos CAPICOM deben crearse mediante CAPICOM.dll. CAPICOM.dll también debe estar presente y registrado en tiempo de ejecución para usar CAPICOM Objects. CAPICOM.dll debe agregarse a Visual Basic referencias de proyectos para usar objetos de CAPICOM.

CAPICOM está disponible como archivo redistribuible que se puede descargar desde [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281). Para obtener información acerca de las versiones de CAPICOM, consulte [versiones de CAPICOM](capicom-versions.md).

**Para registrar CAPICOM.dll**

-   En un símbolo del sistema, cambie el directorio al directorio donde se almacena CAPICOM.dll y, a continuación, escriba el siguiente comando:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Limitaciones de código de ejemplo

Para proporcionar un código más conciso y más legible, los principios de prácticas recomendadas de programación no siempre se siguen en estos ejemplos. En concreto, solo se muestran las respuestas de error limitadas. Las aplicaciones de trabajo siempre deben comprobar los códigos de error devueltos y realizar las acciones adecuadas cuando se produce un error.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Contenedores de claves, claves y certificados necesarios en CAPICOM

Aunque cualquier usuario puede realizar algunas operaciones con objetos CAPICOM en cualquier equipo, crear [*firmas digitales*](../secgloss/d-gly.md) y recuperar el contenido de texto sin formato de un mensaje con doble cifrado mediante CAPICOM objetos son operaciones basadas en certificados. El usuario que crea una firma digital y el usuario que recupera el contenido cifrado de un mensaje con envoltorio debe tener un certificado digital con una clave privada asociada disponible. Si no hay un certificado con una clave privada asociada, se producirá un error en la operación criptográfica. Los usuarios de aplicaciones de CAPICOM deben asegurarse de que tienen el certificado adecuado y la clave privada disponible cuando se ejecutan las aplicaciones.

En algunos ejemplos de las secciones siguientes se realizan operaciones que requieren un [*par de claves pública y privada*](../secgloss/p-gly.md) para cifrar y descifrar archivos, mensajes y firmas. Muchos de estos programas se compilarán y ejecutarán pero producirán errores en tiempo de ejecución sin la existencia de [*contenedores de claves*](../secgloss/k-gly.md), claves, almacenes de certificados y [*certificados*](../secgloss/c-gly.md) adecuados en esos almacenes.

**Para crear un certificado autofirmado**

1.  Instale las herramientas de firma. Se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows, el kit de desarrollo de software (SDK) de la plataforma o el SDK de .NET Framework.
2.  Una vez descargado Makecert.exe, ejecute el siguiente comando en un símbolo del sistema, sustituyendo un nombre de *usuario por nombre* de usuario, un nombre de organización para *NombreDeOrganización* y un nombre de compañía para *CompanyName*:

    **Makecert-r-n "CN =**_username_*_, ou =_*_NombreDeOrganización_*_, o =_*_CompanyName_*_"-SS My_*

3.  El certificado se puede colocar en el almacén My del usuario actual. Importe el certificado creado en el almacén raíz para que sea de confianza.

 

 
