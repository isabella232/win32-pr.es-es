---
title: Escribir servidores y clientes compatibles con versiones anteriores
description: En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación errónea entre los servidores y clientes modificados y sus homólogos implementados.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, compatibilidad con versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55cc3731e75893fa1ab1390769131c3d1ad7263c15b08daebd9049f49f87c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010343"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Escribir servidores y clientes compatibles con versiones anteriores

En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación errónea entre los servidores y clientes modificados y sus homólogos implementados. Sin embargo, en la práctica, los desarrolladores con frecuencia deben introducir cambios en las interfaces existentes sin modificar la versión, ya que los clientes y servidores anteriores deben poder comunicarse con otras nuevas. Se trata de un problema mayor para RPC estándar que para COM; la consulta es una manera natural de buscar interfaces admitidas en COM, mientras que en RPC se debe usar el control de excepciones para una cobertura equivalente.

En esta sección se de abordan los procedimientos recomendados de programación RPC para abordar estas situaciones. Esta sección se divide en los temas siguientes:

-   [Teoría de versiones para RPC y COM](the-versioning-theory-for-rpc-and-com.md)
-   [Cambiar interfaces de una manera compatible con versiones anteriores](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Ejemplos de cambios incompatibles](examples-of-incompatible-changes.md)

 

 




