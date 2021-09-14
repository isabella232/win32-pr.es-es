---
description: Las anotaciones y semánticas estándar (DXSAS) proporcionan un método para usar sombreadores de una manera estándar que permite usar sombreadores con herramientas, aplicaciones y motores de juegos.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: Referencia de semántica y anotaciones estándar de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060667"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>Referencia de semántica y anotaciones estándar de DirectX

Las anotaciones y semánticas estándar (DXSAS) proporcionan un método para usar sombreadores de una manera estándar que permite usar sombreadores con herramientas, aplicaciones y motores de juegos. DXSAS define un conjunto de semánticas y anotaciones que se adjuntan a los valores de aplicación host y parámetros de efecto con el fin de compartir efectos. Para que estas anotaciones y semánticas sean útiles, deben implementarse tanto en la aplicación host como en el archivo de efecto. En este documento se describe el estándar DXSAS, que aprovecha la potencia de DirectX Effect Framework para permitir que las aplicaciones host y las herramientas compartan efectos de DirectX (archivos .fx) mediante programación, así como para diseñar la interacción con la interfaz de usuario.

## <a name="background-information"></a>Información general

Las anotaciones y semánticas estándar están diseñadas para enlazar los parámetros de efecto y archivo X a los valores de la aplicación host. D3DX Effect Framework (o efectos) encapsula el estado de representación. Al encapsular el estado de representación (incluido el estado de procesamiento de vértices, texturas y píxeles) en un efecto, puede crear una biblioteca de efectos que cubre una amplia gama de opciones de representación. Esto puede incluir opciones como la representación en distintos tipos de hardware o la representación con combinación de paso único o múltiple. Para obtener más información sobre la plataforma de efectos, consulte Referencia [de efecto](dx9-graphics-reference-effects.md). DXSAS se basa en este marco, lo que permite una experiencia más coherente para los desarrolladores. Una vez encapsulada la configuración de representación en un efecto, el estándar DXSAS permite al desarrollador del efecto exponer la intención de los parámetros de efecto a través de anotaciones. A continuación, cualquier aplicación o herramienta host (no solo la que se diseñó para usar el efecto) que sea compatible con el estándar comprenderá cómo usar el efecto de la manera que se diseñó.

La normalización del conjunto de anotaciones y semánticas de efecto que admiten las aplicaciones host permite a los autores de efectos crear efectos que se pueden usar en varios proyectos y, por tanto, promover una comunidad más amplia de usuarios de efecto. El estándar DXSAS hace que los desarrolladores puedan leer los archivos, se pueden intercambiar entre herramientas y permite a los desarrolladores aprovechar herramientas de terceros para crear efectos para su canalización.

En este documento se describe el estándar DXSAS, que usa anotaciones para expresar la intención de los parámetros de efecto, así como definir una colección de valores de aplicación host que las aplicaciones host aceptan para que estén disponibles para un efecto.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Creación de efectos con anotaciones estándar y semántica

Como puede ver en el diagrama siguiente, el estándar DXSAS requiere anotaciones en un archivo de efecto, así como una aplicación host que siga las instrucciones descritas aquí para trabajar con el archivo.

![diagrama del estándar dxsas para aplicaciones host y archivos de efecto](images/sas-2.png)

La aplicación host debe implementar la lógica de la interfaz de usuario y el entorno de host. Para implementar efectos compatibles con DXSAS, lea los temas siguientes:

-   El [parámetro global](global-parameter.md) define la información pertinente para el efecto, como la versión o el autor del efecto.
-   [Enlace de](data-binding.md) datos define la colección de parámetros (así como su tipo y estructura) que puede usar un efecto que puede establecer la aplicación host expuesta a efectos.
-   Para asociar un control de interfaz de usuario a un parámetro de efecto, use una anotación [de interfaz de usuario](ui-annotation.md). Estas anotaciones incluyen: [SasUiMax,](ui-annotation.md) [SasUiMin,](ui-annotation.md) [SasUiSteps,](ui-annotation.md) [SasUiStepsPower](ui-annotation.md)y [SasUiStride.](ui-annotation.md)
-   Para inicializar un parámetro de efecto con los datos contenidos en un archivo externo, use una [anotación de inicialización de parámetros](parameter-initialization-annotation.md).
-   Cuando se transfieren datos entre la aplicación host y un efecto (o [viceversa),](casting-and-conversion.md) la conversión y la conversión se producirán cuando los tipos no coincidan exactamente. En esta sección se especifica cómo se escriben los datos cuando los tipos de origen y de destino difieren. Además, use [ParameterValueModifiers](casting-and-conversion.md) para modificar cómo la aplicación host debe interpretar los datos leídos del parámetro de efecto. Estas anotaciones incluyen: [SasNormalize](casting-and-conversion.md) y [SasUnits.](casting-and-conversion.md)

## <a name="case-sensitivity"></a>Distinción entre mayúsculas y minúsculas

Todos los identificadores, la semántica y los valores de anotación no tienen distinción entre mayúsculas y minúsculas. Los nombres de anotación (no los valores) distinguen mayúsculas de minúsculas. El sistema de efectos D3DX reconoce los nombres de anotación y, por tanto, también los nombres de anotación SAS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efecto](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



