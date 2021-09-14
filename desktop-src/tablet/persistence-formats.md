---
description: Una aplicación debe ser capaz de generar y consumir datos de varios formatos.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formatos de persistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8edd88a4b170d2299832a205d80dc6704aea66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361020"
---
# <a name="persistence-formats"></a>Formatos de persistencia

Una aplicación debe ser capaz de generar y consumir datos de varios formatos. A menudo incluyen formatos binarios propietarios y también deben incluir algunos formatos estándar, como formato de texto enriquecido (RTF) o HTML.

En la tabla siguiente se enumeran algunos formatos que pueden contener entrada de lápiz.



| Formato                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Las aplicaciones deben usar el formato serializado de entrada de lápiz (ISF) para codificar la entrada de lápiz en sus formatos binarios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Se recomienda encarecidamente un formato HTML para la representación de contenido heterogéneo. Las aplicaciones deben usar archivos Formato de intercambio de gráficos (GIF) para codificar la entrada de lápiz en sus documentos HTML. Para obtener más información sobre los GIF con notificaciones, vea [Bloques de creación](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Imagen<br/>                            | En el caso de las aplicaciones para las que no hay ninguna otra intersección de compatibilidad, una aplicación habilitada para lápiz debe mover imágenes con formato de mapa de bits y metarchivo al Portapapeles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Formato serializado de tinta (ISF)<br/>      | El formato ISF es la representación más compacta y persistente de la entrada de lápiz. Aunque a menudo contiene solo datos de entrada de lápiz, ISF es extensible. Las aplicaciones pueden establecer atributos personalizados (identificados por un identificador único global (GUID)) en un objeto [**Ink,**](inkdisp-class.md) un trazo de lápiz o un punto de entrada de lápiz. Esto le permite almacenar cualquier tipo de datos o metadatos como atributo en una secuencia de ISF. Para la interoperabilidad del Portapapeles, la entrada de lápiz se puede colocar en una ranura estándar del Portapapeles para ISF que se define en los archivos de encabezado del Kit de desarrollo de software (SDK).<br/> ISF es un formato específico de microsoft Tablet PC Technology y solo se admite en los métodos Load y [**Save del objeto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) [**Ink.**](inkdisp-class.md) [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)<br/> |
| RTF<br/>                              | Es posible generar un formato de Portapapeles RTF y codificar la entrada manuscrita en RTF como objetos OLE. Esto permite pegar la entrada de lápiz en un contenedor OLE, como Microsoft Word o una aplicación basada en RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Lenguaje de marcado extensible (XML)<br/> | Las aplicaciones pueden usar cualquiera de los formatos de entrada de lápiz codificados en base 64 para almacenar la entrada de lápiz en un formato de archivo XML. Un formato XML es útil para escribir contenido de entrada de lápiz en una base de datos, como en el caso de un campo de firma, o incluso como formato de archivo principal de aplicaciones. Esto mitiga la necesidad de escribir un analizador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




