---
title: Escritura de clientes y servidores compatibles con versiones anteriores
description: En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación indebido entre los servidores y los clientes modificados y sus homólogos implementados.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC (llamada a procedimiento remoto), procedimientos recomendados, compatibilidad con versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148785"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Escritura de clientes y servidores compatibles con versiones anteriores

En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación indebido entre los servidores y los clientes modificados y sus homólogos implementados. Sin embargo, en la práctica, los desarrolladores deben introducir cambios en las interfaces existentes sin modificar la versión, ya que los clientes y servidores anteriores deben ser capaces de comunicarse con otros nuevos. Se trata de un problema mayor para RPC estándar que para COM; la consulta es una forma natural de buscar interfaces compatibles en COM, mientras que en el control de excepciones RPC debe usarse para una cobertura equivalente.

En esta sección se describen las mejores prácticas de programación de RPC para abordar estas situaciones. Esta sección se divide en los temas siguientes:

-   [La teoría de control de versiones de RPC y COM](the-versioning-theory-for-rpc-and-com.md)
-   [Cambiar las interfaces de una manera compatible con versiones anteriores](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Ejemplos de cambios incompatibles](examples-of-incompatible-changes.md)

 

 




