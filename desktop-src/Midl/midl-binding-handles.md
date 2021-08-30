---
title: Identificadores de enlace MIDL
description: Los identificadores de enlace son objetos de datos que representan el enlace entre el cliente y el servidor.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipos de datos MIDL, identificadores de enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ca39a8d5a75b392692460ae8268bf60ad19824193060639fef5f9ffe87832d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869635"
---
# <a name="midl-binding-handles"></a>Identificadores de enlace MIDL

Los identificadores de enlace son objetos de datos que representan el enlace entre el cliente y el servidor.

MIDL admite el identificador de tipo base [**\_ t**](handle-t.md). Los identificadores de este tipo se conocen como "identificadores primitivos".

Puede definir sus propios tipos de identificador mediante el **\[ atributo handle. \]** Los identificadores definidos de esta manera se conocen como identificadores "definidos por el usuario" o "personalizados" o "genéricos".

También puede definir un identificador que mantenga la información de estado mediante el atributo **\[** [**de identificador \_ de**](context-handle.md) **\]** contexto. Los identificadores definidos de esta manera se conocen como identificadores de "contexto".

Si no se necesita información de estado y no elige llamar a las bibliotecas en tiempo de ejecución rpc para administrar el identificador, puede solicitar que las bibliotecas en tiempo de ejecución proporcionen enlace automático. Esto se hace mediante el control automático de la palabra clave ACF **\[** [**\_**](auto-handle.md) **\]** .

Puede especificar una variable global como identificador de enlace mediante el identificador implícito de la palabra clave ACF **\[** [**\_**](implicit-handle.md) **\]** . La **\[ palabra clave \_ handle \]** explícita se usa para especificar que cada función remota tiene un identificador especificado explícitamente.

Para obtener más información, vea [Enlace y identificadores](/windows/desktop/Rpc/binding-and-handles).

 

 