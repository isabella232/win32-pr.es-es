---
description: En Microsoft Media Foundation, una cola de trabajo es una manera eficaz de realizar operaciones asincrónicas en otro subproceso.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Colas de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277070"
---
# <a name="work-queues"></a>Colas de trabajo

En Microsoft Media Foundation, una cola de trabajo es una manera eficaz de realizar operaciones asincrónicas en otro subproceso.

Esta sección contiene los temas siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="using-work-queues.md">Uso de colas de trabajo</a></td>
<td>Describe cómo una aplicación o un componente puede usar colas de trabajo para realizar operaciones asincrónicas.</td>
</tr>
<tr class="even">
<td><a href="writing-an-asynchronous-method.md">Escribir un método asincrónico</a></td>
<td>Describe cómo escribir un método asincrónico que sigue el patrón Begin/end descrito en métodos de <a href="asynchronous-callback-methods.md">devolución de llamada asincrónica</a>.</td>
</tr>
<tr class="odd">
<td><a href="custom-asynchronous-result-objects.md">Objetos de resultado asincrónicos personalizados</a></td>
<td>Describe cómo crear una implementación personalizada de la interfaz <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .<br/>
<blockquote>
[!Note]<br />
La mayoría de las aplicaciones deben usar la implementación estándar que proporciona <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>. Este tema está destinado a aplicaciones con requisitos avanzados.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="media-foundation-work-queue-and-threading-improvements.md">Mejoras en la cola de trabajo y subprocesos</a></td>
<td>Describe las mejoras en Windows 8 para los subprocesos y las colas de trabajo en la plataforma Media Foundation.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 




