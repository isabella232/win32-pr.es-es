---
title: Inconvenientes
description: Inconvenientes
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532391"
---
# <a name="disadvantages"></a>Inconvenientes

Los servidores en proceso proporcionan la velocidad y el tamaño de un controlador de objetos con la funcionalidad de edición de un servidor local. ¿Por qué alguna vez elegiría implementar la aplicación OLE como un servidor local en lugar de un servidor en proceso? Hay varias razones:

-   Seguridad. Solo un servidor local tiene el espacio de direcciones aislado del cliente. Un servidor de tipo en curso comparte el espacio de direcciones y el contexto del proceso del cliente y, por tanto, puede ser menos sólido en caso de que se produzcan errores o la programación malintencionada.
-   Granularidad. Un servidor local puede hospedar varias instancias de su objeto en muchos clientes diferentes, compartiendo el estado del servidor entre objetos en varios clientes de maneras que serían difíciles o imposibles si se implementan como un servidor en proceso, que es simplemente un archivo DLL cargado en cada cliente.
-   Compatibilidad. Si decide implementar un servidor en proceso, se renuncia a la compatibilidad con OLE 1, que no es compatible con estos servidores. Esto no será una consideración para muchos desarrolladores, pero si es así, es de importancia crítica.
-   Imposibilidad de admitir vínculos. Un servidor en proceso no puede servir como origen de vínculo. Dado que un archivo DLL no se puede ejecutar por sí mismo, no puede crear un objeto de archivo al que se vinculará.

A pesar de estas desventajas, un servidor en proceso puede ser una opción excelente para su velocidad y tamaño, si se ajusta a todos los demás requisitos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ventajas](advantages.md)
</dt> <dt>

[Servidores en proceso](in-process-servers.md)
</dt> </dl>

 

 




