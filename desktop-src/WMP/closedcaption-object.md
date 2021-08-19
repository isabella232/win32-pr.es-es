---
title: ClosedCaption (objeto)
description: El objeto ClosedCaption proporciona una manera de incluir subtítulos con un clip multimedia. El texto de subtítulos se encuentra en un archivo de intercambio de medios accesibles sincronizado (SAMI).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- ClosedCaption Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10ae51af31e724bd066dbbb9e826569da40159460eb1e7bf570aea331dff86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119606"
---
# <a name="closedcaption-object"></a>ClosedCaption (objeto)

El **objeto ClosedCaption** proporciona una manera de incluir subtítulos con un clip multimedia. El texto de subtítulos se encuentra en un archivo de intercambio de medios accesibles sincronizado (SAMI).

El **objeto ClosedCaption** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Especifica o recupera el nombre del marco o control que muestra los subtítulos.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Especifica o recupera el nombre del archivo que contiene la información necesaria para el subtítulo. |
| [SAMILang](closedcaption-samilang.md)             | Especifica o recupera el idioma que se muestra para los subtítulos.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Recupera el número de idiomas admitidos por el archivo SAMI actual.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Especifica o recupera el estilo de subtítulos.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Recupera el número de estilos admitidos por el archivo SAMI actual.                                   |



 

El **objeto ClosedCaption** admite los métodos siguientes.



| Método                                                 | Descripción                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Recupera el nombre de un idioma admitido por el archivo SAMI actual.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Recupera el nombre de un estilo admitido por el archivo SAMI actual.                        |



 

Se **tiene acceso al objeto ClosedCaption** a través de la propiedad siguiente.



| Object                      | Propiedad                                  |
|-----------------------------|-------------------------------------------|
| [Reproductor](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




