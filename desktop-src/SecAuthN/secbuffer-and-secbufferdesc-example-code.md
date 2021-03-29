---
description: En este ejemplo se muestra cómo inicializar una matriz de búferes de seguridad.
ms.assetid: f8196a9c-786a-49a3-85a4-1bd5f414a653
title: Código de ejemplo de SecBuffer y SecBufferDesc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7d28e885d6eec65c209caeda299b2f7e5f2ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667116"
---
# <a name="secbuffer-and-secbufferdesc-example-code"></a><span data-ttu-id="01a15-103">Código de ejemplo de SecBuffer y SecBufferDesc</span><span class="sxs-lookup"><span data-stu-id="01a15-103">SecBuffer and SecBufferDesc Example Code</span></span>

<span data-ttu-id="01a15-104">En este ejemplo se muestra cómo inicializar una matriz de búferes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="01a15-104">This example demonstrates how to initialize an array of security buffers.</span></span> <span data-ttu-id="01a15-105">Muestra los búferes de seguridad de entrada inicializados por el lado del servidor de una conexión para preparar una llamada a [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="01a15-105">It shows input security buffers initialized by the server side of a connection to prepare for a call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span> <span data-ttu-id="01a15-106">Tenga en cuenta que el último búfer contiene el token de seguridad opaco recibido por el cliente y que la \_ marca ReadOnly SECBUFFER está establecida en [**SECBUFFER**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).</span><span class="sxs-lookup"><span data-stu-id="01a15-106">Note that the last buffer contains the opaque security token received by the client and that the SECBUFFER\_READONLY flag is set on [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).</span></span>


```C++
SecBuffer  Buffers[3];
SecBufferDesc BufferDesc;
BYTE *pHeader;
BYTE *pMessage;
BYTE *pTrailer;

//--------------------------------------------------------------------
// pHeader, pMessage, and pTrailer are BYTE strings.
// In a working program, they would be assigned string values.

BufferDesc.ulVersion = SECBUFFER_VERSION;
BufferDesc.cBuffers = 3;
BufferDesc.pBuffers = Buffers;

Buffers[0].cbBuffer = sizeof(pHeader);
Buffers[0].BufferType = SECBUFFER_READONLY | SECBUFFER_DATA;
Buffers[0].pvBuffer = pHeader;

Buffers[1].cbBuffer = sizeof(pMessage);
Buffers[1].BufferType = SECBUFFER_DATA;
Buffers[1].pvBuffer = pMessage;

Buffers[2].cbBuffer = sizeof(pTrailer);
Buffers[2].BufferType = SECBUFFER_READONLY | SECBUFFER_TOKEN;
Buffers[2].pvBuffer = pTrailer;
```



 

 
