---
description: Las anotaciones y la semántica estándar (DXSAS) proporcionan un método para usar sombreadores de forma estándar que permiten usar los sombreadores con herramientas, aplicaciones y motores de juegos.
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: Referencia de las anotaciones y semánticas estándar de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495023"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a>Referencia de las anotaciones y semánticas estándar de DirectX

Las anotaciones y la semántica estándar (DXSAS) proporcionan un método para usar sombreadores de forma estándar que permiten usar los sombreadores con herramientas, aplicaciones y motores de juegos. DXSAS define un conjunto de semánticas y anotaciones que se adjuntan a los valores de la aplicación host y los parámetros de efecto con el fin de compartir efectos. Para que estas anotaciones y semánticas sean útiles, deben implementarse en la aplicación host y en el archivo de efecto. En este documento se describe el estándar DXSAS que aprovecha la eficacia del marco de trabajo de DirectX para permitir que las aplicaciones y herramientas host compartan los efectos de DirectX (archivos. FX) mediante programación, así como para diseñar la interacción con la interfaz de usuario.

## <a name="background-information"></a>Información general

Las anotaciones estándar y las semánticas están diseñadas para enlazar los parámetros de efectos y archivos X para hospedar los valores de la aplicación. El marco de efecto de D3DX (o efectos) encapsula el estado de representación. Al encapsular el estado de representación (incluido el estado de procesamiento de vértices, texturas y píxeles) en un efecto, puede crear una biblioteca de efectos que cubran una amplia gama de opciones de representación. Esto podría incluir opciones como la representación en diferentes tipos de hardware, o la representación con una mezcla de una o varias pases. Para obtener más información sobre el marco de trabajo de efecto, debe consultar la [referencia de efectos](dx9-graphics-reference-effects.md). DXSAS se basa en este marco de trabajo, lo que permite una experiencia más coherente para los desarrolladores. Una vez que el programa de instalación de representación está encapsulado en un efecto, el estándar DXSAS permite al desarrollador de efectos exponer la intención de los parámetros de efecto mediante anotaciones. Después, estas anotaciones pueden ser leídas por cualquier aplicación o herramienta host (no solo por la que se diseñó para usar el efecto) que sea compatible con el estándar y aprenderá a usar el efecto de la manera que se diseñó.

La estandarización del conjunto de la semántica de efectos y las anotaciones que admiten las aplicaciones permiten a los autores de efectos crear efectos que se pueden usar en varios proyectos y, por tanto, promocionar una comunidad más amplia de usuarios de efecto. El estándar DXSAS hace que los archivos sean legibles por los desarrolladores, que se pueden intercambiar entre herramientas, y permite a los desarrolladores aprovechar herramientas de terceros para crear efectos para su canalización.

En este documento se describe el estándar DXSAS que usa anotaciones para expresar la intención de los parámetros de efectos, así como la definición de una colección de valores de aplicación host que hospedan aplicaciones que aceptan poner a disposición de un efecto.

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a>Efectos de creación con anotaciones y semánticas estándar

Como puede ver en el diagrama siguiente, el estándar DXSAS requiere anotaciones en un archivo de efectos, así como una aplicación host que sigue las instrucciones que se describen aquí para trabajar con el archivo.

![diagrama del estándar dxsas para aplicaciones host y archivos de efectos](images/sas-2.png)

La aplicación host debe implementar la lógica de la interfaz de usuario y el entorno de host. Para implementar los efectos compatibles con DXSAS, lea los temas siguientes:

-   El [parámetro global](global-parameter.md) define la información pertinente para el efecto, como la versión o el autor del efecto.
-   El [enlace de datos](data-binding.md) define la colección de parámetros (así como su tipo y estructura) que puede usar un efecto que se puede establecer mediante la aplicación host expuesta a efectos.
-   Para asociar un control de la interfaz de usuario a un parámetro de efecto, use una [anotación de interfaz](ui-annotation.md)de usuario. Estas anotaciones incluyen: [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md)y [SasUiStride](ui-annotation.md).
-   Para inicializar un parámetro de efecto con los datos contenidos en un archivo externo, use una [anotación de inicialización de parámetro](parameter-initialization-annotation.md).
-   Cuando los datos se transfieren entre la aplicación host y un efecto (o viceversa), se producirá la [conversión y la conversión](casting-and-conversion.md) cuando los tipos no coincidan exactamente. En esta sección se especifica cómo se escriben los datos cuando los tipos de origen y de destino difieren. Además, use [ParameterValueModifiers](casting-and-conversion.md) para modificar el modo en que la aplicación host debe interpretar los datos leídos del parámetro Effect. Estas anotaciones incluyen: [SasNormalize](casting-and-conversion.md) y [SasUnits](casting-and-conversion.md).

## <a name="case-sensitivity"></a>Distinción entre mayúsculas y minúsculas

Todos los identificadores, semánticas y valores de anotación no distinguen mayúsculas de minúsculas. Los nombres de anotación (no valores) distinguen mayúsculas de minúsculas. Los nombres de anotación son reconocidos por el sistema de efectos de D3DX y, por lo tanto, los nombres de anotación SAS también lo son.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de efectos](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



