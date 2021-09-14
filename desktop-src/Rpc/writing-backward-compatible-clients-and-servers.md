---
title: Escribir clientes y servidores compatibles con versiones anteriores
description: En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación errónea entre los servidores y clientes modificados y sus homólogos implementados.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, compatibilidad con versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071365"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Escribir clientes y servidores compatibles con versiones anteriores

En teoría, el esquema de control de versiones de RPC ayuda a evitar la comunicación errónea entre los servidores y clientes modificados y sus homólogos implementados. Sin embargo, en la práctica, los desarrolladores deben introducir con frecuencia cambios en las interfaces existentes sin modificar la versión, ya que los clientes y servidores anteriores deben poder comunicarse con otras nuevas. Se trata de un problema mayor para RPC estándar que para COM; la consulta es una manera natural de buscar interfaces admitidas en COM, mientras que en el control de excepciones RPC debe usarse para una cobertura equivalente.

En esta sección se de abordan los procedimientos recomendados de programación RPC para abordar estas situaciones. Esta sección se divide en los temas siguientes:

-   [Teoría del control de versiones para RPC y COM](the-versioning-theory-for-rpc-and-com.md)
-   [Cambiar interfaces de una manera compatible con versiones anteriores](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Ejemplos de cambios incompatibles](examples-of-incompatible-changes.md)

 

 




