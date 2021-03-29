---
title: Procesamiento de dominios y manipulación de atributos
description: El procesamiento de los territorios, que también se conoce como manipulación de atributos, hace referencia a la transformación del nombre del usuario que solicita el acceso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792574"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Procesamiento de dominios y manipulación de atributos

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

El procesamiento de los territorios, que también se conoce como manipulación de atributos, hace referencia a la transformación del nombre del usuario que solicita el acceso. También se puede manipular el identificador de la estación de llamada y el identificador de estación llamada. Las reglas de procesamiento de dominios forman parte de la colección de atributos de Perfil de proxy.

Para cada manipulación, debe crear dos atributos [de regla de manipulación](/windows/desktop/Nps/sdo-manipulation-rule) . Cada uno de estos atributos es un valor de cadena. La primera regla contiene una expresión regular que representa el patrón que debe coincidir. La segunda regla contiene una expresión regular que representa el texto de reemplazo. También debe crear un atributo [de destino de manipulación](/windows/desktop/Nps/sdo-manipulation-target) . Este atributo es una enumeración que especifica qué parte de la información del usuario se va a manipular.

Es importante el orden en el que se crean los atributos. NPS procesa los atributos en el orden en que se crearon.

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

[Atributos compatibles con SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Creación de una directiva de solicitud de conexión](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 