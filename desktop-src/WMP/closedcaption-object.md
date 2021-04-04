---
title: Objeto ClosedCaption
description: El objeto ClosedCaption proporciona una manera de incluir leyendas con un clip multimedia. El texto de la leyenda se encuentra en un archivo de intercambio de medios accesibles (SAMI) sincronizado.
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Objeto ClosedCaption Media Player de Windows
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076967"
---
# <a name="closedcaption-object"></a>Objeto ClosedCaption

El objeto **ClosedCaption** proporciona una manera de incluir leyendas con un clip multimedia. El texto de la leyenda se encuentra en un archivo de intercambio de medios accesibles (SAMI) sincronizado.

El objeto **ClosedCaption** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Especifica o recupera el nombre del marco o control que muestra los subtítulos.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Especifica o recupera el nombre del archivo que contiene la información necesaria para los subtítulos (CC). |
| [SAMILang](closedcaption-samilang.md)             | Especifica o recupera el idioma que se muestra para los subtítulos (CC).                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Recupera el número de idiomas admitidos por el archivo SAMI actual.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Especifica o recupera el estilo de subtítulos (CC).                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Recupera el número de estilos admitidos por el archivo SAMI actual.                                   |



 

El objeto **ClosedCaption** admite los siguientes métodos.



| Método                                                 | Descripción                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Recupera el nombre de un idioma admitido por el archivo SAMI actual.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Recupera el nombre de un estilo compatible con el archivo SAMI actual.                        |



 

Se tiene acceso al objeto **ClosedCaption** a través de la propiedad siguiente.



| Object                      | Propiedad                                  |
|-----------------------------|-------------------------------------------|
| [Reproductor](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




