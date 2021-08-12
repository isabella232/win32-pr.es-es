---
title: Procesamiento de dominios y manipulación de atributos
description: El procesamiento de dominios, que también se conoce como manipulación de atributos, hace referencia a la transformación del nombre del usuario que solicita acceso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8054ad8234ca4772a52619d83bc85a9d357f2cf8da2f1c969eed918c75a8305a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618951"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Procesamiento de dominios y manipulación de atributos

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

El procesamiento de dominios, que también se conoce como manipulación de atributos, hace referencia a la transformación del nombre del usuario que solicita acceso. También se pueden manipular el identificador de la estación de llamada y el identificador de la estación llamada. Las reglas de procesamiento de dominios forman parte de la colección de atributos de perfil de proxy.

Para cada manipulación, debe crear dos atributos [manipulation-rule.](/windows/desktop/Nps/sdo-manipulation-rule) Cada uno de estos atributos es un valor de cadena. La primera regla contiene una expresión regular que representa el patrón que se debe coincidir. La segunda regla contiene una expresión regular que representa el texto de reemplazo. También debe crear un atributo [Manipulation-Target.](/windows/desktop/Nps/sdo-manipulation-target) Este atributo es una enumeración que especifica qué parte de la información del usuario se va a manipular.

El orden en el que se crean los atributos es importante. NPS procesa los atributos en el orden en que se crearon.

En la tabla siguiente se muestra un ejemplo de un conjunto de atributos de manipulación.



| Nombre                 | Tipo         | Valor de cadena     |
|----------------------|--------------|------------------|
| msManipulationRule   | **VT \_ BSTR** | "@company.com"   |
| msManipulationRule   | **VT \_ BSTR** | "@microsoft.com" |
| msManipulationRule   | **VT \_ BSTR** | "^.+@"           |
| msManipulationRule   | **VT \_ BSTR** | "guest@"         |
| msManipulationTarget | **VT \_ I4**   | "1"              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Jerarquía del modelo de objetos](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Atributos admitidos por SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Creación de una directiva de solicitud de conexión](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 