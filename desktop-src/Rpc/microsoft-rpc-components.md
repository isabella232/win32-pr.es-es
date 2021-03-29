---
title: Componentes de RPC
description: Componentes de llamada a procedimiento remoto (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC llamada a procedimiento remoto, descripción, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994282"
---
# <a name="rpc-components"></a>Componentes de RPC

RPC incluye los componentes principales siguientes:

-   Compilador MIDL
-   Bibliotecas en tiempo de ejecución y archivos de encabezado
-   Proveedor de servicios de nombres (a veces conocido como localizador)
-   Asignador de extremos (a veces denominado asignador de puertos)

En el modelo RPC, puede especificar formalmente una interfaz para los procedimientos remotos mediante un lenguaje diseñado para este fin. Este lenguaje se denomina lenguaje de definición de interfaz o IDL. La implementación de Microsoft de este lenguaje se denomina Lenguaje de definición de interfaz de Microsoft, o MIDL.

Después de crear una interfaz, debe pasarla a través del compilador de MIDL. Este compilador genera los códigos auxiliares que traducen las llamadas a procedimientos locales en llamadas a procedimientos remotos. Los códigos auxiliares son funciones de marcador de posición que realizan las llamadas a las funciones de la biblioteca en tiempo de ejecución, que administran la llamada a procedimiento remoto. La ventaja de este enfoque es que la red es casi completamente transparente para la aplicación distribuida. El programa cliente llama a lo que parece ser un procedimiento local; el trabajo de convertirlos en llamadas remotas se realiza automáticamente. Todo el código que traduce los datos, accede a la red y recupera los resultados se generan automáticamente mediante el compilador de MIDL y es invisible para la aplicación.

 

 




