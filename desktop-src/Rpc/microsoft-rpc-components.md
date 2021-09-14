---
title: Componentes de RPC
description: Componentes de llamada a procedimiento remoto (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Llamada a procedimiento remoto RPC , descrito, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244437"
---
# <a name="rpc-components"></a>Componentes de RPC

RPC incluye los siguientes componentes principales:

-   Compilador MIDL
-   Bibliotecas en tiempo de ejecución y archivos de encabezado
-   Proveedor de servicios de nombres (a veces denominado localizador)
-   Asignador de puntos de conexión (a veces denominado asignador de puertos)

En el modelo RPC, puede especificar formalmente una interfaz para los procedimientos remotos mediante un lenguaje diseñado para este propósito. Este lenguaje se denomina Lenguaje de definición de interfaz o IDL. La implementación de Microsoft de este lenguaje se denomina Lenguaje de definición de interfaz de Microsoft o MIDL.

Después de crear una interfaz, debe pasarla a través del compilador MIDL. Este compilador genera los códigos auxiliares que convierten las llamadas de procedimiento local en llamadas a procedimiento remoto. Los códigos auxiliares son funciones de marcador de posición que hacen las llamadas a las funciones de la biblioteca en tiempo de ejecución, que administran la llamada a procedimiento remoto. La ventaja de este enfoque es que la red se vuelve casi completamente transparente para la aplicación distribuida. El programa cliente llama a lo que parecen ser procedimientos locales. El trabajo de convertirlas en llamadas remotas se realiza automáticamente. El compilador MIDL genera automáticamente todo el código que traduce los datos, accede a la red y recupera los resultados y es invisible para la aplicación.

 

 




