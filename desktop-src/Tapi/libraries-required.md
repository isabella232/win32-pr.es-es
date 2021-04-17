---
description: A continuación se muestra una lista de los archivos. lib necesarios para compilar varias aplicaciones TAPI 3, desde 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Bibliotecas requeridas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677481"
---
# <a name="libraries-required"></a><span data-ttu-id="34878-103">Bibliotecas requeridas</span><span class="sxs-lookup"><span data-stu-id="34878-103">Libraries Required</span></span>

<span data-ttu-id="34878-104">Una lista de archivos. lib necesarios para compilar varias aplicaciones TAPI 3, desde 1/22/01:</span><span class="sxs-lookup"><span data-stu-id="34878-104">A list of .lib files required to compile various TAPI 3 applications, as of 1/22/01:</span></span>

-   <span data-ttu-id="34878-105">Advapi32. lib</span><span class="sxs-lookup"><span data-stu-id="34878-105">Advapi32.lib</span></span>
-   <span data-ttu-id="34878-106">Amstrmid. lib (GUID de ActiveMovie)</span><span class="sxs-lookup"><span data-stu-id="34878-106">Amstrmid.lib (ActiveMovie GUIDs)</span></span>
-   <span data-ttu-id="34878-107">Kernel32.lib</span><span class="sxs-lookup"><span data-stu-id="34878-107">Kernel32.lib</span></span>
-   <span data-ttu-id="34878-108">Mdhcpid. lib (GUID de multidifusión)</span><span class="sxs-lookup"><span data-stu-id="34878-108">Mdhcpid.lib (multicast GUIDs)</span></span>
-   <span data-ttu-id="34878-109">Ole32. lib (COM)</span><span class="sxs-lookup"><span data-stu-id="34878-109">Ole32.lib (COM)</span></span>
-   <span data-ttu-id="34878-110">Oleaut32. lib (automatización COM)</span><span class="sxs-lookup"><span data-stu-id="34878-110">Oleaut32.lib (COM Automation)</span></span>
-   <span data-ttu-id="34878-111">Rendid. lib (GUID de encuentro)</span><span class="sxs-lookup"><span data-stu-id="34878-111">Rendid.lib (Rendezvous GUIDs)</span></span>
-   <span data-ttu-id="34878-112">Rpcndr. lib</span><span class="sxs-lookup"><span data-stu-id="34878-112">Rpcndr.lib</span></span>
-   <span data-ttu-id="34878-113">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="34878-113">Rpcns4.lib</span></span>
-   <span data-ttu-id="34878-114">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="34878-114">Rpcrt4.lib</span></span>
-   <span data-ttu-id="34878-115">Sdpblbid. lib (GUID del Protocolo de descriptor de sesión (SDP))</span><span class="sxs-lookup"><span data-stu-id="34878-115">Sdpblbid.lib (Session Descriptor Protocol (SDP) GUIDs)</span></span>
-   <span data-ttu-id="34878-116">Strmiids. lib</span><span class="sxs-lookup"><span data-stu-id="34878-116">Strmiids.lib</span></span>
-   <span data-ttu-id="34878-117">User32. lib</span><span class="sxs-lookup"><span data-stu-id="34878-117">User32.lib</span></span>
-   <span data-ttu-id="34878-118">UUID. lib</span><span class="sxs-lookup"><span data-stu-id="34878-118">Uuid.lib</span></span>
-   <span data-ttu-id="34878-119">Wldap32. lib</span><span class="sxs-lookup"><span data-stu-id="34878-119">Wldap32.lib</span></span>
-   <span data-ttu-id="34878-120">Ws2 \_ 32. lib</span><span class="sxs-lookup"><span data-stu-id="34878-120">Ws2\_32.lib</span></span>

<span data-ttu-id="34878-121">Si usa Microsoft Visual Studio, es posible que tenga que actualizar la versión.</span><span class="sxs-lookup"><span data-stu-id="34878-121">If you are using Microsoft Visual Studio, you may need to update your version.</span></span> <span data-ttu-id="34878-122">En concreto, Link.exe debe llevar una fecha 3/19/98 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34878-122">In particular, Link.exe must carry a date of 3/19/98 or later.</span></span>

<span data-ttu-id="34878-123">La definición del compilador debe incluir \_ Win32 \_ WinNT establecido en al menos 0x500 y \_ Win32 \_ DCOM.</span><span class="sxs-lookup"><span data-stu-id="34878-123">Compiler defines must include \_WIN32\_WINNT set to at least 0x500 and \_WIN32\_DCOM.</span></span>

 

 



