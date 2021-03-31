---
title: Identificadores de enlace MIDL
description: Los identificadores de enlace son objetos de datos que representan el enlace entre el cliente y el servidor.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipos de datos MIDL, identificadores de enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077584"
---
# <a name="midl-binding-handles"></a>Identificadores de enlace MIDL

Los identificadores de enlace son objetos de datos que representan el enlace entre el cliente y el servidor.

MIDL admite el identificador de tipo base [**\_ t**](handle-t.md). Los identificadores de este tipo se conocen como "identificadores primitivos".

Puede definir sus propios tipos de identificador mediante el atributo **\[ Handle \]** . Los identificadores definidos de esta manera se conocen como identificadores "definidos por el usuario" o "personalizados" o "genéricos".

También puede definir un identificador que mantenga la información de estado mediante el atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** . Los identificadores definidos de esta manera se conocen como identificadores de "contexto".

Si no se necesita información de estado y no elige llamar a las bibliotecas en tiempo de ejecución de RPC para administrar el identificador, puede solicitar que las bibliotecas en tiempo de ejecución proporcionen enlaces automáticos. Esto se hace mediante la palabra clave ACF de **\[** [**\_ identificador automático**](auto-handle.md) **\]** .

Puede especificar una variable global como identificador de enlace mediante el uso del **\[** [**\_ identificador implícito**](implicit-handle.md)de la palabra clave ACF **\]** . La palabra clave de **\[ \_ identificador \] explícito** se usa para indicar que cada función remota tiene un identificador especificado explícitamente.

Para obtener más información, vea [enlazar y controlar](/windows/desktop/Rpc/binding-and-handles).

 

 