---
description: Agregar nodos de salida con TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Agregar nodos de salida con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e975e332a464218f8629363f34a2d3fbef0e5a49
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481981"
---
# <a name="adding-output-nodes-with-topoedit"></a>Agregar nodos de salida con TopoEdit

En una topología, un nodo de salida representa un receptor multimedia que recibe datos multimedia de un nodo de transformación y los presenta para su reproducción. El tipo de nodo de salida depende del tipo de medio del nodo de origen.

En la tabla siguiente se muestra el comando de menú o barra de herramientas para agregar un nodo de salida a la topología.




| Tipo de medio de origen | Menú o comando de barra de herramientas | Descripción | 
|-------------------|----------------------|-------------|
| Secuencia de audio | En el <strong>menú Topología,</strong> haga clic <strong>en Agregar SAR.</strong> | Crea un nodo de salida para el representador de audio de streaming (SAR) que reproduce una secuencia de audio a través de un dispositivo de audio, como una tarjeta de sonido. | 
| Secuencia de vídeo | En el <strong>menú Topología,</strong> haga clic <strong>en Agregar EVR.</strong> | Crea un nodo de salida para el representador de vídeo mejorado (EVR) que muestra fotogramas para una secuencia de vídeo. | 
| Receptor multimedia personalizado | <ol><li>En el <strong>menú Topología,</strong> haga clic <strong>en Agregar receptor personalizado.</strong><br /> Se abre <strong>el cuadro de diálogo GUID</strong> personalizado de entrada.<br /></li><li><p>En el <strong>campo GUID:</strong> , escriba el GUID del receptor personalizado que desea agregar a la topología.<br /></p><blockquote>[!Note]<br />TopoEdit espera el GUID con el formato "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". De lo contrario, no se puede agregar el nodo y se muestra un mensaje de error "GUID no válido".</blockquote><p><br /></p></li><li>Haga clic en <strong>Aceptar</strong>.<br /></li></ol> | Crea un nodo de salida para el receptor de flujo para un origen multimedia personalizado.<br /> El receptor personalizado debe admitir <strong>CoCreateInstance</strong> para que el receptor se pueda especificar con un CLSID.<br /> | 




 

TopoEdit crea el nodo de salida especificado. El **panel Topología muestra** el nodo de salida como un cuadro verde que muestra el nombre del receptor de flujo.

Para obtener información sobre cómo agregar nodos de salida mediante programación mediante Media Foundation API, vea [Crear nodos de salida.](creating-output-nodes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




