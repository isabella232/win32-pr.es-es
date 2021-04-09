---
description: En esta guía se proporciona la información necesaria para permitir que la aplicación Microsoft Windows use la próxima generación de protocolo de Internet, versión 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guía de IPv6 para aplicaciones de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154272"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="03149-103">Guía de IPv6 para aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="03149-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="03149-104">En esta guía se proporciona la información necesaria para permitir que la aplicación Microsoft Windows use la próxima generación de protocolo de Internet, versión 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="03149-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="03149-105">Agregar funcionalidad IPv6 a la aplicación no es necesariamente un proceso de portabilidad.</span><span class="sxs-lookup"><span data-stu-id="03149-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="03149-106">Para trasladar una aplicación, se recomienda modificar el código para que funcione en una plataforma diferente, lo que implica la salida de la plataforma anterior.</span><span class="sxs-lookup"><span data-stu-id="03149-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="03149-107">Esta guía está específicamente estructurada para ayudar a agregar funcionalidad IPv6 a una aplicación a la vez que se conserva la funcionalidad de IPv4.</span><span class="sxs-lookup"><span data-stu-id="03149-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="03149-108">En esta guía se describen los problemas asociados con la adición de la funcionalidad IPv6 y, a continuación, se destinan a las áreas de desarrollo más afectadas por la transición.</span><span class="sxs-lookup"><span data-stu-id="03149-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="03149-109">Cada área recibe una explicación detallada de los problemas que se deben tener en cuidado, las estrategias sugeridas para evitarlos y sugerencias sobre cómo hacer el mejor uso de los nuevos elementos de programación de [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funciones y estructuras).</span><span class="sxs-lookup"><span data-stu-id="03149-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="03149-110">Para obtener información adicional sobre IPv6, consulte [compatibilidad con IPv6](ipv6-support-2.md).</span><span class="sxs-lookup"><span data-stu-id="03149-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="03149-111">En esta guía también se proporcionan ejemplos de código para ofrecerle experiencia práctica y representaciones visuales de los problemas que podría encontrar al modificar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="03149-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="03149-112">Los ejemplos provienen de ejemplos completos y funcionales de una sencilla aplicación de Windows Sockets que se ha modificado para admitir tanto IPv4 como IPv6.</span><span class="sxs-lookup"><span data-stu-id="03149-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="03149-113">El código fuente de estos ejemplos de trabajo se incluye en su totalidad en dos apéndices al final de este documento: [apéndice a: el código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md) incluye el código fuente de una aplicación antes de que se modifique para admitir IPv6; [Apéndice B: código fuente independiente de la versión de IP](appendix-b-ip-version-agnostic-source-code-2.md) proporciona el código fuente una vez que la aplicación se ha habilitado para IPv6.</span><span class="sxs-lookup"><span data-stu-id="03149-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="03149-114">Microsoft proporciona una utilidad llamada Checkv4.exe que le ayuda a encontrar código potencialmente sensible a la migración en el código de la aplicación y también hace recomendaciones para las correcciones.</span><span class="sxs-lookup"><span data-stu-id="03149-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="03149-115">La utilidad de Checkv4.exe se muestra en este documento, mediante la aplicación de ejemplo incluida en los apéndices, junto con las capturas de pantalla que muestran la salida que produce la utilidad de Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="03149-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="03149-116">Para obtener más información, vea [usar la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="03149-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="03149-117">Las áreas de programación que se tratan en esta guía son:</span><span class="sxs-lookup"><span data-stu-id="03149-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="03149-118">Cambiar las estructuras de datos para IPv6 Winsock Appications</span><span class="sxs-lookup"><span data-stu-id="03149-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="03149-119">Llamadas de función para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="03149-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="03149-120">Uso de direcciones IPv4 codificadas</span><span class="sxs-lookup"><span data-stu-id="03149-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="03149-121">Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="03149-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="03149-122">Protocolos subyacentes para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="03149-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="03149-123">Sockets de doble pila para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="03149-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="03149-124">Dado que no hay ninguna secuencia uniforme de eventos, las secciones que abordan los problemas de habilitación de IPv6 no se organizan de forma secuencial, por lo que puede hacer referencia a cualquier sección en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="03149-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="03149-125">Se recomienda encarecidamente que revise cada sección mientras agrega funcionalidad IPv6 a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="03149-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="03149-126">También es aconsejable leer sobre la utilidad de Checkv4.exe, ya que incluye sugerencias sobre el orden en que se deben tratar los problemas de habilitación de IPv6.</span><span class="sxs-lookup"><span data-stu-id="03149-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="03149-127">Para consultar la utilidad de Checkv4.exe y revisar el orden en el que debe abordar el proceso de portabilidad de las aplicaciones, consulte [usar la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="03149-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="03149-128">En esta sección se incluye información sobre una marca de tiempo de compilación que comprueba estrictamente si hay elementos de programación incompatibles con IPv6.</span><span class="sxs-lookup"><span data-stu-id="03149-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="03149-129">Para ir directamente a la aplicación de ejemplo, vea el [Apéndice A: código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md) y [Apéndice B: código fuente independiente de la versión de IP](appendix-b-ip-version-agnostic-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="03149-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03149-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03149-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03149-131">Protocolo de Internet versión 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="03149-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="03149-132">Compatibilidad con IPv6</span><span class="sxs-lookup"><span data-stu-id="03149-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="03149-133">IPv6 Technology Preview para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="03149-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="03149-134">Usar la utilidad Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="03149-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="03149-135">Apéndice A: código fuente solo IPv4</span><span class="sxs-lookup"><span data-stu-id="03149-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="03149-136">Apéndice B: código fuente independiente de la versión de IP</span><span class="sxs-lookup"><span data-stu-id="03149-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



