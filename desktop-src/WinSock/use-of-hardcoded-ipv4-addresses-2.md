---
description: La longevidad de IPv4 dio lugar a codificar de forma rígida muchas direcciones IPv4 conocidas, como las direcciones de bucle invertido (127. x.x. x), constantes enteras como la indirección \_ de bucle invertido, entre otras.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso de direcciones IPv4 codificadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360290"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="ac20f-103">Uso de direcciones IPv4 codificadas</span><span class="sxs-lookup"><span data-stu-id="ac20f-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="ac20f-104">La longevidad de IPv4 dio lugar a codificar de forma rígida muchas direcciones IPv4 conocidas, como las direcciones de bucle invertido (127. x.x. x), constantes enteras como la indirección \_ de bucle invertido, entre otras.</span><span class="sxs-lookup"><span data-stu-id="ac20f-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="ac20f-105">La práctica de codificar de forma rígida estas direcciones presenta problemas obvios al modificar una aplicación existente para admitir IPv6 o crear nuevos programas independientes de la versión de IP.</span><span class="sxs-lookup"><span data-stu-id="ac20f-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="ac20f-106">Procedimiento recomendado</span><span class="sxs-lookup"><span data-stu-id="ac20f-106">Best Practice</span></span>

-   <span data-ttu-id="ac20f-107">El mejor enfoque es evitar codificar cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="ac20f-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="ac20f-108">Código que se debe evitar</span><span class="sxs-lookup"><span data-stu-id="ac20f-108">Code To Avoid</span></span>

-   <span data-ttu-id="ac20f-109">Evite el uso de direcciones codificadas en código.</span><span class="sxs-lookup"><span data-stu-id="ac20f-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="ac20f-110">**Para modificar la base de código existente de IPv4 a IPv4 e IPv6: interoperabilidad**</span><span class="sxs-lookup"><span data-stu-id="ac20f-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="ac20f-111">Adquiera la utilidad *Checkv4.exe* .</span><span class="sxs-lookup"><span data-stu-id="ac20f-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="ac20f-112">La utilidad de *Checkv4.exe* se instala como parte del kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ac20f-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="ac20f-113">El Windows SDK está disponible a través de una suscripción a MSDN y también se puede descargar desde el sitio web de Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="ac20f-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="ac20f-114">Ejecute la utilidad *Checkv4.exe* en el código.</span><span class="sxs-lookup"><span data-stu-id="ac20f-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="ac20f-115">Obtenga información acerca de cómo ejecutar la utilidad *Checkv4.exe* en los archivos de la sección sobre [el uso de la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="ac20f-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="ac20f-116">La utilidad de *Checkv4.exe* le alerta de la presencia de definiciones comunes para las direcciones IPv4, como la indirección de \_ bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="ac20f-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="ac20f-117">Modifique cualquier código que use cadenas literales con código independiente de la versión del protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac20f-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="ac20f-118">Busque en el código base otras posibles cadenas literales, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ac20f-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="ac20f-119">La utilidad *Checkv4.exe* puede ayudarle a encontrar cadenas literales comunes, pero puede haber otros que sean específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac20f-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="ac20f-120">Debe realizar búsquedas y pruebas exhaustivas para asegurarse de que el código base ha erradicado los posibles problemas asociados a las cadenas literales.</span><span class="sxs-lookup"><span data-stu-id="ac20f-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac20f-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac20f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac20f-122">Guía de IPv6 para aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="ac20f-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="ac20f-123">Cambiar las estructuras de datos para IPv6 Winsock Appications</span><span class="sxs-lookup"><span data-stu-id="ac20f-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="ac20f-124">Sockets de doble pila para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="ac20f-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="ac20f-125">Llamadas de función para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="ac20f-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="ac20f-126">Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="ac20f-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="ac20f-127">Protocolos subyacentes para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="ac20f-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



