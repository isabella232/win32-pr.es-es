---
title: Identificadores implícitos frente a identificadores explícitos
description: Para declarar un identificador de serialización, use el identificador de tipo de identificador primitivo \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244629"
---
# <a name="implicit-vs-explicit-handles"></a>Identificadores implícitos frente a identificadores explícitos

Para declarar un identificador de serialización, use el identificador de tipo de [**identificador primitivo \_ t**](/windows/desktop/Midl/handle-t). Los identificadores de serialización pueden ser explícitos o implícitos. Especifique identificadores implícitos en el ACF de la aplicación mediante el **\[ atributo de \_ identificador \]** implícito. El compilador MIDL generará una variable de identificador de serialización global. Los procedimientos de serialización con un identificador implícito usan esta variable global para tener acceso a un contexto de serialización válido.

Al usar la codificación de tipos, las rutinas generadas que admiten la serialización de un tipo determinado usan el identificador implícito global para acceder al contexto de serialización. Tenga en cuenta que es posible que las rutinas remotas necesiten usar el identificador implícito como identificador de enlace. Asegúrese de que el identificador implícito está establecido en un identificador de serialización válido antes de realizar una llamada de serialización.

Un identificador explícito se especifica como un parámetro del prototipo del procedimiento de serialización en el archivo IDL, o también se puede especificar mediante el atributo **\[ de \_ \]** identificador explícito en el ACF. El parámetro de identificador explícito se usa para establecer el contexto de serialización adecuado para el procedimiento. Para establecer el contexto correcto en el caso de la serialización de tipos, el compilador genera las rutinas auxiliares que usan el parámetro [**\_ t**](/windows/desktop/Midl/handle-t) de identificador explícito como identificador de serialización. Debe proporcionar un identificador de serialización válido al llamar a una rutina de compatibilidad de tipo de serialización o procedimiento de serialización.

 

 