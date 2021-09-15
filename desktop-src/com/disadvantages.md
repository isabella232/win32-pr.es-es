---
title: Inconvenientes
description: Inconvenientes
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359385"
---
# <a name="disadvantages"></a>Inconvenientes

Los servidores en proceso proporcionan la ventaja de velocidad y tamaño de un controlador de objetos con la funcionalidad de edición de un servidor local. ¿Por qué elegiría alguna vez implementar la aplicación OLE como un servidor local en lugar de un servidor en proceso? Hay varias razones:

-   Seguridad. Solo un servidor local tiene su espacio de direcciones aislado del del cliente. Un servidor en proceso comparte el espacio de direcciones y el contexto de proceso del cliente y, por tanto, puede ser menos sólido frente a errores o programación malintencionada.
-   Granularidad. Un servidor local puede hospedar varias instancias de su objeto en muchos clientes diferentes, compartiendo el estado del servidor entre objetos de varios clientes de maneras que serían difíciles o imposibles si se implementa como un servidor en proceso, que es simplemente un archivo DLL cargado en cada cliente.
-   Compatibilidad. Si decide implementar un servidor en proceso, se relinquish la compatibilidad con OLE 1, que no admite dichos servidores. Esto no será una consideración para muchos desarrolladores, pero si es así, es una preocupación crítica.
-   Incapacidad de admitir vínculos. Un servidor en proceso no puede actuar como origen de vínculo. Puesto que un archivo DLL no se puede ejecutar por sí mismo, no puede crear un objeto de archivo al que se va a vincular.

A pesar de estas desventajas, un servidor en proceso puede ser una opción excelente para su velocidad y tamaño, si se ajusta a todos los demás requisitos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ventajas](advantages.md)
</dt> <dt>

[Servidores en proceso](in-process-servers.md)
</dt> </dl>

 

 




