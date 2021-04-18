---
description: El número máximo de sockets admitidos por un proveedor de servicios de Windows Sockets determinado es específico de la implementación.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Número máximo de sockets admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715118"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="a5598-103">Número máximo de sockets admitidos</span><span class="sxs-lookup"><span data-stu-id="a5598-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="a5598-104">El número máximo de sockets admitidos por un proveedor de servicios de Windows Sockets determinado es específico de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a5598-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="a5598-105">El proveedor de Microsoft Winsock limita el número máximo de sockets admitidos solo por la memoria disponible en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a5598-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="a5598-106">Sin embargo, los proveedores de Winsock de terceros pueden tener limitaciones en cuanto a los números de sockets compatibles.</span><span class="sxs-lookup"><span data-stu-id="a5598-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="a5598-107">Una aplicación no debe hacer suposiciones sobre la disponibilidad de un determinado número de Sockets.</span><span class="sxs-lookup"><span data-stu-id="a5598-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="a5598-108">Para obtener más información sobre este tema, vea [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span><span class="sxs-lookup"><span data-stu-id="a5598-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="a5598-109">FD \_ set y SELECT</span><span class="sxs-lookup"><span data-stu-id="a5598-109">FD\_SET and select</span></span>

<span data-ttu-id="a5598-110">\_En el archivo de encabezado *WinSock2. h* se definen varias macros de FD XXX para su uso en la migración de aplicaciones a Windows desde el entorno de Unix.</span><span class="sxs-lookup"><span data-stu-id="a5598-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="a5598-111">Estas macros se utilizan con las funciones [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) y [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) para la migración de aplicaciones a Windows.</span><span class="sxs-lookup"><span data-stu-id="a5598-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="a5598-112">El número máximo de sockets que puede usar una aplicación de Windows Sockets no se ve afectado por la constante del manifiesto FD \_ setSize.</span><span class="sxs-lookup"><span data-stu-id="a5598-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="a5598-113">Este valor definido en el archivo de encabezado *WinSock2. h* se usa para construir las [**estructuras \_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) utilizadas con la función **Select** .</span><span class="sxs-lookup"><span data-stu-id="a5598-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="a5598-114">El valor predeterminado en WinSock2. h es 64.</span><span class="sxs-lookup"><span data-stu-id="a5598-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="a5598-115">Si una aplicación está diseñada para ser capaz de trabajar con más de 64 Sockets mediante las funciones **Select** y **WSAPoll** , el implementador debe definir el manifiesto FD \_ en cada archivo de código fuente antes de incluir el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="a5598-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="a5598-116">Una forma de hacerlo puede ser incluir la definición dentro de las opciones del compilador en el archivo make.</span><span class="sxs-lookup"><span data-stu-id="a5598-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="a5598-117">Por ejemplo, puede Agregar "-DFD \_ setSize = 128" como una opción a la línea de comandos del compilador de Microsoft C++.</span><span class="sxs-lookup"><span data-stu-id="a5598-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="a5598-118">Se debe resaltar que \_ la definición de FD setSize como un valor determinado no tiene ningún efecto en el número real de sockets que proporciona un proveedor de servicios de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a5598-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="a5598-119">Este valor solo afecta a las \_ macros FD XXX usadas por las funciones **Select** y **WSAPoll** .</span><span class="sxs-lookup"><span data-stu-id="a5598-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5598-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5598-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5598-121">**FD ( \_ conjunto)**</span><span class="sxs-lookup"><span data-stu-id="a5598-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="a5598-122">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="a5598-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="a5598-123">**no**</span><span class="sxs-lookup"><span data-stu-id="a5598-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="a5598-124">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="a5598-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="a5598-125">**WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="a5598-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="a5598-126">**WSAPoll**</span><span class="sxs-lookup"><span data-stu-id="a5598-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
