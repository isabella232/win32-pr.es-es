---
title: Identificadores implícitos frente a controladores explícitos
description: Para declarar un identificador de serialización, utilice el identificador de tipo de identificador primitivo \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904765"
---
# <a name="implicit-vs-explicit-handles"></a>Identificadores implícitos frente a controladores explícitos

Para declarar un identificador de serialización, utilice el identificador de tipo de identificador primitivo [**\_ t**](/windows/desktop/Midl/handle-t). Los identificadores de serialización pueden ser explícitos o implícitos. Especifique identificadores implícitos en el ACF de la aplicación mediante el atributo de **\[ \_ identificador \] implícito** . El compilador MIDL generará una variable global de identificador de serialización. Los procedimientos de serialización con un identificador implícito utilizan esta variable global para tener acceso a un contexto de serialización válido.

Al utilizar la codificación de tipos, las rutinas generadas que admiten la serialización de un tipo determinado usan el identificador implícito global para tener acceso al contexto de serialización. Tenga en cuenta que las rutinas remotas pueden necesitar usar el identificador implícito como un identificador de enlace. Asegúrese de que el identificador implícito esté establecido en un identificador de serialización válido antes de realizar una llamada de serialización.

Un identificador explícito se especifica como un parámetro del prototipo del procedimiento de serialización en el archivo IDL, o también se puede especificar mediante el atributo de **\[ \_ identificador \] explícito** en el ACF. El parámetro de identificador explícito se utiliza para establecer el contexto de serialización adecuado para el procedimiento. Para establecer el contexto correcto en el caso de la serialización de tipos, el compilador genera las rutinas auxiliares que utilizan el parámetro de [**identificador explícito \_ t**](/windows/desktop/Midl/handle-t) como identificador de serialización. Debe proporcionar un identificador de serialización válido al llamar a un procedimiento de serialización o a una rutina de compatibilidad de tipo de serialización.

 

 