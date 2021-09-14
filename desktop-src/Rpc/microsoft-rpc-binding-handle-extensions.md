---
title: Extensiones de Binding-Handle RPC de Microsoft
description: Las extensiones de Microsoft para el lenguaje IDL admiten varios parámetros de identificador que aparecen en posiciones distintas del primer parámetro situado más a la izquierda.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c93b68b20628bf6f7f65cee026412846e0b497d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244442"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Extensiones de Binding-Handle RPC de Microsoft

Las extensiones de Microsoft para el lenguaje IDL admiten varios parámetros de identificador que aparecen en posiciones distintas del primer parámetro situado más a la izquierda. En los pasos siguientes se describe la secuencia por la que pasa el compilador MIDL para resolver el parámetro binding-handle en modo de compatibilidad con DCE (/**osf)** y en modo predeterminado (extendido por Microsoft).

## <a name="dce-compatibility-mode"></a>Modo de compatibilidad de DCE

-   Identificador de enlace que aparece en la primera posición.
-   Situado más a \[ [**la izquierda en**](/windows/desktop/Midl/in), parámetro de identificador [**\_ de**](/windows/desktop/Midl/context-handle) \] contexto.
-   Identificador de enlace implícito especificado por \[ [**el identificador \_ implícito**](/windows/desktop/Midl/implicit-handle) \] o el identificador \[ [**\_ automático**](/windows/desktop/Midl/auto-handle) \] .
-   Si no hay ningún ACF presente, use de forma predeterminada \[ **el identificador \_ automático** \] .

## <a name="default-mode"></a>Modo predeterminado

-   Identificador de enlace explícito más a la izquierda.
-   Identificador de enlace implícito especificado por \[ [**el identificador \_ implícito**](/windows/desktop/Midl/implicit-handle) \] o el identificador \[ [**\_ automático**](/windows/desktop/Midl/auto-handle) \] .
-   Si no hay ningún ACF presente, use de forma predeterminada \[ [**el identificador \_ automático**](/windows/desktop/Midl/auto-handle) \] .

Los compiladores IDL de DCE buscan un identificador de enlace explícito como primer parámetro. Cuando el primer parámetro no es un identificador de enlace y se especifican uno o varios identificadores de contexto, se usa el identificador de contexto situado más a la izquierda como identificador de enlace. Cuando el primer parámetro no es un identificador y no hay identificadores de contexto, el procedimiento usa el enlace implícito mediante el identificador implícito del atributo ACF o \[ [**\_**](/windows/desktop/Midl/implicit-handle) el \] identificador \[ [**\_ automático**](/windows/desktop/Midl/auto-handle) \] .

Las extensiones de Microsoft para el IDL permiten que el identificador de enlace esté en una posición que no sea el primer parámetro. El control situado más a la izquierda en el parámetro de identificador explícito(ya sea un identificador primitivo, definido por el programador o de \[ [](/windows/desktop/Midl/in) \] contexto) es el identificador de enlace. Cuando no hay parámetros de identificador, el procedimiento usa el enlace implícito mediante el identificador implícito del atributo ACF o el \[ [**\_**](/windows/desktop/Midl/implicit-handle) \] identificador \[ [**\_ automático**](/windows/desktop/Midl/auto-handle) \] .

Las reglas siguientes se aplican al modo de compatibilidad con DCE (/osf) y al modo predeterminado:

-   El enlace de identificador automático se usa cuando no hay ningún ACF presente.
-   Los \[ [**identificadores**](/windows/desktop/Midl/in) de entrada o de entrada explícitos de una \] función individual \[  [](/windows/desktop/Midl/out-idl) \] adelantan cualquier enlace implícito especificado para la interfaz .
-   No \[ [**se**](/windows/desktop/Midl/in) \] \[ **admiten varios identificadores** primitivos de entrada \] o de entrada.
-   Se \[ [**permiten**](/windows/desktop/Midl/in) \] varios \[ **identificadores** \] de contexto explícitos dentro o en .
-   Todos los parámetros de identificador definidos por el programador, excepto el parámetro binding-handle, se tratan como datos transmisibles.

La tabla siguiente contiene ejemplos y describe cómo se asignan los identificadores de enlace en cada modo del compilador.




| Ejemplo | Descripción | 
|---------|-------------|
| <pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre> | No se especifica ningún identificador explícito. Se usa el identificador de enlace implícito, especificado por [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] o [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>]. Cuando no hay ACF, se usa un identificador automático. | 
| <pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,           [in] short s );</code></pre> | Se especifica un identificador explícito handle_t tipo . El parámetro <em>H</em> es el identificador de enlace para el procedimiento. | 
| <pre class="syntax" data-space="preserve"><code>void proc3([in] short s,           [in] handle_t H );</code></pre> | El primer parámetro no es un identificador. En el modo predeterminado, el parámetro de identificador situado más a la izquierda, <em>H</em>, es el identificador de enlace. En el modo /osf, se usa el enlace implícito. Se notifica un error porque se espera que el segundo parámetro sea transmisible y handle_t no se pueda transmitir. | 
| <pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;void proc1([in] short s,           [in] MY_HDL H );</code></pre> | El primer parámetro no es un identificador. En el modo predeterminado, el parámetro de identificador situado más a la izquierda, <em>H</em>, es el identificador de enlace. Los códigos auxiliares llaman a las rutinas proporcionadas por el MY_HDL_bind y MY_HDL_unbind. En el modo in/osf, se usa el enlace implícito. El parámetro de identificador definido por el <em>programador H</em> se trata como datos transmisibles. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;void proc1([in] MY_HDL H,            [in] MY_HDL p );</code></pre> | El primer parámetro es un identificador de enlace. El parámetro <em>H</em> es el parámetro binding-handle. El segundo parámetro de identificador definido por el programador se trata como datos transmisibles. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [context_handle] void * CTXT_HDL;void proc1([in] short s,           [in] long l,           [in] CTXT_HDL H ,           [in] char c);</code></pre> | El identificador de enlace es un identificador de contexto. El parámetro <em>H</em> es el identificador de enlace. | 




 

 

 
