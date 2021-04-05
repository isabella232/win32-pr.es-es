---
title: Extensiones de Binding-Handle de Microsoft RPC
description: Las extensiones de Microsoft para el lenguaje IDL admiten varios parámetros de identificador que aparecen en posiciones distintas del primer parámetro, más a la izquierda.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078515"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Extensiones de Binding-Handle de Microsoft RPC

Las extensiones de Microsoft para el lenguaje IDL admiten varios parámetros de identificador que aparecen en posiciones distintas del primer parámetro, más a la izquierda. En los pasos siguientes se describe la secuencia con la que pasa el compilador de MIDL para resolver el parámetro de identificador de enlace en modo de compatibilidad de DCE (/**OSF**) y en modo predeterminado (Microsoft-Extended).

## <a name="dce-compatibility-mode"></a>Modo de compatibilidad de DCE

-   Identificador de enlace que aparece en la primera posición.
-   El \[ parámetro de [**\_ identificador de contexto**](/windows/desktop/Midl/context-handle) [**en**](/windows/desktop/Midl/in)el extremo izquierdo \] .
-   Identificador de enlace implícito especificado por el identificador \[ [**implícito \_**](/windows/desktop/Midl/implicit-handle) \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .
-   Si no hay ningún ACF presente, el valor predeterminado es usar el \[ **\_ controlador automático** \] .

## <a name="default-mode"></a>Modo predeterminado

-   Identificador de enlace explícito más a la izquierda.
-   Identificador de enlace implícito especificado por el identificador \[ [**implícito \_**](/windows/desktop/Midl/implicit-handle) \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .
-   Si no hay ningún ACF presente, el valor predeterminado es usar el \[ [**\_ controlador automático**](/windows/desktop/Midl/auto-handle) \] .

Los compiladores de DCE IDL buscan un identificador de enlace explícito como primer parámetro. Cuando el primer parámetro no es un identificador de enlace y se especifican uno o más identificadores de contexto, se usa el identificador de contexto situado más a la izquierda como identificador de enlace. Cuando el primer parámetro no es un identificador y no hay identificadores de contexto, el procedimiento utiliza el enlace implícito mediante el \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) del atributo ACF \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .

Las extensiones de Microsoft para el IDL permiten que el controlador de enlace esté en una posición distinta del primer parámetro. El extremo izquierdo \[ [**en**](/windows/desktop/Midl/in) el \] parámetro de identificador explícito, ya sea un identificador primitivo, definido por el programador o el contexto, es el identificador de enlace. Cuando no hay ningún parámetro de identificador, el procedimiento utiliza el enlace implícito mediante el \[ [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) del atributo ACF \] o el \[ [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] .

Las siguientes reglas se aplican al modo de compatibilidad con DCE (/OSF) y al modo predeterminado:

-   El enlace de control automático se utiliza cuando no hay ACF.
-   \[ [](/windows/desktop/Midl/in) \] \[ Los identificadores [**out**](/windows/desktop/Midl/out-idl) in o **in**, out explícitos \] para una función individual tienen preferencia sobre cualquier enlace implícito especificado para la interfaz.
-   \[ [](/windows/desktop/Midl/in) \] \[  \] No se admiten varios identificadores primitivos en o en.
-   \[ [](/windows/desktop/Midl/in) \] \[  \] Se permiten varios identificadores de contexto explícitos en o en.
-   Todos los parámetros de identificador definidos por el programador, excepto el parámetro de identificador de enlace, se tratan como datos transmisibles.

La tabla siguiente contiene ejemplos y describe cómo se asignan los identificadores de enlace en cada modo del compilador.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ejemplo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td>No se especifica ningún identificador explícito. Se utiliza el identificador de enlace implícito, especificado por [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] o [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>]. Cuando no hay ACF, se usa un identificador automático.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td>Se especifica un identificador explícito de tipo handle_t. El parámetro <em>H</em> es el identificador de enlace para el procedimiento.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td>El primer parámetro no es un identificador. En el modo predeterminado, el parámetro de identificador de la izquierda, <em>H</em>, es el identificador de enlace. En modo/OSF, se usa el enlace implícito. Se ha detectado un error porque se espera que el segundo parámetro sea transmisible y handle_t no se puede transmitir.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td>El primer parámetro no es un identificador. En el modo predeterminado, el parámetro de identificador de la izquierda, <em>H</em>, es el identificador de enlace. El código auxiliar llama a las rutinas proporcionadas por el usuario MY_HDL_bind y MY_HDL_unbind. En el modo/OSF, se usa el enlace implícito. El parámetro de identificador definido por el programador <em>H</em> se trata como datos transmisibles.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td>El primer parámetro es un identificador de enlace. El parámetro <em>H</em> es el parámetro de identificador de enlace. El segundo parámetro de identificador definido por el programador se trata como datos transmisibles.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td>El identificador de enlace es un identificador de contexto. El parámetro <em>H</em> es el identificador de enlace.</td>
</tr>
</tbody>
</table>



 

 

 