---
description: Una aplicación debe ser capaz de generar y consumir datos de varios formatos.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formatos de persistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8edd88a4b170d2299832a205d80dc6704aea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697551"
---
# <a name="persistence-formats"></a>Formatos de persistencia

Una aplicación debe ser capaz de generar y consumir datos de varios formatos. Suelen incluir formatos binarios propietarios y también deben incluir algunos formatos estándar, como el formato de texto enriquecido (RTF) o HTML.

En la tabla siguiente se muestran algunos formatos que pueden contener entradas manuscritas.



| Formato                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Las aplicaciones deben usar el formato serializado de entrada de lápiz (ISF) para codificar la entrada manuscrita en sus formatos binarios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Se recomienda un formato HTML para la representación de contenido heterogéneo. Las aplicaciones deben usar el formato de intercambio de gráficos enriquecido (GIF) para codificar la entrada manuscrita en sus documentos HTML. Para obtener más información sobre los archivos GIF enriquecidos, vea [bloques de creación](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Imagen<br/>                            | En el caso de las aplicaciones para las que no hay ninguna otra intersección de compatibilidad, una aplicación habilitada para tinta debe trasladar las imágenes con formato de mapa de bits y metarchivo al portapapeles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Formato serializado de tinta (ISF)<br/>      | El formato ISF es la representación más compacta y persistente de la entrada de lápiz. Aunque a menudo solo contiene datos de tinta, ISF es extensible. Las aplicaciones pueden establecer atributos personalizados (identificados mediante un identificador único global (GUID)) en un objeto de [**entrada manuscrita**](inkdisp-class.md) , trazo de tinta o punto de entrada. Esto le permite almacenar cualquier tipo de datos o metadatos como un atributo en una secuencia ISF. Para la interoperabilidad del portapapeles, la entrada manuscrita se puede colocar en una ranura de Portapapeles estándar para ISF que se define en los archivos de encabezado del kit de desarrollo de software (SDK).<br/> ISF es un formato específico de la tecnología de Tablet PC de Microsoft y solo se admite en los métodos de [**carga**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) y [**guardado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) del objeto de [**entrada de lápiz**](inkdisp-class.md) .<br/> |
| RTF<br/>                              | Es posible generar un formato de Portapapeles RTF y codificar la entrada manuscrita en RTF como objetos OLE. Esto permite pegar la entrada manuscrita en un contenedor OLE, como Microsoft Word o una aplicación basada en RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Lenguaje de marcado extensible (XML)<br/> | Las aplicaciones pueden usar uno de los formatos de tinta que están codificados en base-64 para almacenar entradas manuscritas en formato de archivo XML. Un formato XML es útil para especificar el contenido de la tinta en una base de datos, como en el caso de un campo de firma, o incluso como un formato de archivo principal de las aplicaciones. Esto evita la necesidad de escribir un analizador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




