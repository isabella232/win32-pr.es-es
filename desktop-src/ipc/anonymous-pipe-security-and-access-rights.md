---
description: Puede especificar un descriptor de seguridad para una canalización anónima cuando llame a la función CreatePipe. El descriptor de seguridad controla el acceso a los extremos de lectura y escritura de la canalización.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Seguridad de canalización anónima y derechos de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688521"
---
# <a name="anonymous-pipe-security-and-access-rights"></a><span data-ttu-id="517de-104">Seguridad de canalización anónima y derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="517de-104">Anonymous Pipe Security and Access Rights</span></span>

<span data-ttu-id="517de-105">La seguridad de Windows le permite controlar el acceso a las canalizaciones anónimas.</span><span class="sxs-lookup"><span data-stu-id="517de-105">Windows security enables you to control access to anonymous pipes.</span></span> <span data-ttu-id="517de-106">Para obtener más información sobre la seguridad, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="517de-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="517de-107">Puede especificar un [descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors) para una canalización cuando llame a la función [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) .</span><span class="sxs-lookup"><span data-stu-id="517de-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a pipe when you call the [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function.</span></span> <span data-ttu-id="517de-108">El descriptor de seguridad controla el acceso a los extremos de lectura y escritura de la canalización.</span><span class="sxs-lookup"><span data-stu-id="517de-108">The security descriptor controls access to both the read and write ends of the pipe.</span></span> <span data-ttu-id="517de-109">Si especifica **null**, la canalización obtiene un descriptor de seguridad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="517de-109">If you specify **NULL**, the pipe gets a default security descriptor.</span></span> <span data-ttu-id="517de-110">Las ACL del descriptor de seguridad predeterminado para una canalización proceden del token principal o de suplantación del creador.</span><span class="sxs-lookup"><span data-stu-id="517de-110">The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="517de-111">Para recuperar el descriptor de seguridad de una canalización, llame a la función [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="517de-111">To retrieve a pipe's security descriptor, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="517de-112">Para cambiar el descriptor de seguridad de una canalización, llame a la función [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="517de-112">To change a pipe's security descriptor, call the [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="517de-113">La función [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) devuelve dos identificadores para la canalización anónima: un controlador de lectura con acceso genérico de \_ lectura y sincronización, y un identificador de escritura con \_ acceso de escritura y sincronización genéricos.</span><span class="sxs-lookup"><span data-stu-id="517de-113">The [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function returns two handles to the anonymous pipe: a read handle with GENERIC\_READ and SYNCHRONIZE access; and a write handle with GENERIC\_WRITE and SYNCHRONIZE access.</span></span> <span data-ttu-id="517de-114">\_Los accesos genéricos de lectura y \_ escritura usan la misma asignación de derechos de acceso que para las canalizaciones con nombre.</span><span class="sxs-lookup"><span data-stu-id="517de-114">GENERIC\_READ and GENERIC\_WRITE access use the same access rights mapping as for named pipes.</span></span>

<span data-ttu-id="517de-115">El \_ acceso de lectura genérico para una canalización anónima combina los derechos para leer los datos de la canalización, leer los atributos de la canalización, leer atributos extendidos y leer la DACL de la canalización.</span><span class="sxs-lookup"><span data-stu-id="517de-115">GENERIC\_READ access for an anonymous pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.</span></span>

<span data-ttu-id="517de-116">\_El acceso de escritura genérico para una canalización anónima combina los derechos para escribir datos en la canalización, anexar datos a él, escribir atributos de canalización, escribir atributos extendidos y leer la DACL de la canalización.</span><span class="sxs-lookup"><span data-stu-id="517de-116">GENERIC\_WRITE access for an anonymous pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL.</span></span>

 

 
