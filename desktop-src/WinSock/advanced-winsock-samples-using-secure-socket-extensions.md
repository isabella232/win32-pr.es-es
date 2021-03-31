---
description: Ejemplos avanzados de Winsock con extensiones de socket seguras
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Ejemplos avanzados de Winsock con extensiones de socket seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001145"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="65177-103">Ejemplos avanzados de Winsock con extensiones de socket seguras</span><span class="sxs-lookup"><span data-stu-id="65177-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="65177-104">Ejemplo de cliente y servidor TCP seguro</span><span class="sxs-lookup"><span data-stu-id="65177-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="65177-105">En el kit de desarrollo de software (SDK) de Microsoft Windows se incluye un ejemplo de Winsock más avanzado que muestra el uso de extensiones de sockets seguros.</span><span class="sxs-lookup"><span data-stu-id="65177-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="65177-106">El ejemplo incluye un cliente TCP y un servidor que se conectan de forma segura mediante las extensiones Winsock y socket seguro.</span><span class="sxs-lookup"><span data-stu-id="65177-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="65177-107">De forma predeterminada, el código fuente de ejemplo de Winsock se instala en el directorio siguiente:</span><span class="sxs-lookup"><span data-stu-id="65177-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="65177-108">*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ NetDs \\ Winsock*</span><span class="sxs-lookup"><span data-stu-id="65177-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="65177-109">Un ejemplo se encuentra en la siguiente carpeta:</span><span class="sxs-lookup"><span data-stu-id="65177-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="65177-110">*securesocket*</span><span class="sxs-lookup"><span data-stu-id="65177-110">*securesocket*</span></span>

<span data-ttu-id="65177-111">El código de ejemplo se divide en directorios independientes, tal y como se describe a continuación:</span><span class="sxs-lookup"><span data-stu-id="65177-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="65177-112">stcpclient: la carpeta que contiene el código de cliente TCP seguro.</span><span class="sxs-lookup"><span data-stu-id="65177-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="65177-113">stcpcommon: la carpeta que contiene el código de biblioteca común que se comparte entre el cliente y el servidor TCP seguros.</span><span class="sxs-lookup"><span data-stu-id="65177-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="65177-114">stcpserver: la carpeta que contiene el código de servidor TCP seguro.</span><span class="sxs-lookup"><span data-stu-id="65177-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="65177-115">Se debe observar que los ejemplos están diseñados para ejecutarse en dos equipos diferentes que ejecutan Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="65177-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="65177-116">Además, las credenciales de IPsec se deben aprovisionar en ambos equipos para que la conexión se realice correctamente, ya que el ejemplo utiliza IPsec para proteger su tráfico.</span><span class="sxs-lookup"><span data-stu-id="65177-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="65177-117">Consulte la documentación sobre la [configuración de IPSec](/windows/desktop/FWP/ipsec-configuration) para obtener más información sobre cómo configurar las credenciales de IPSec.</span><span class="sxs-lookup"><span data-stu-id="65177-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="65177-118">Al compilar el ejemplo se generarán dos archivos ejecutables:</span><span class="sxs-lookup"><span data-stu-id="65177-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="65177-119">*stcpclient.exe* y *stcpserver.exe*.</span><span class="sxs-lookup"><span data-stu-id="65177-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="65177-120">Copie *stcpclient.exe* en el equipo a y copie *stcpserver.exe* en el equipo B. En el equipo B, inicie el servidor TCP; para ello, ejecute lo siguiente en un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="65177-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="65177-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="65177-121">**stcpserver.exe**</span></span>

<span data-ttu-id="65177-122">Ejecute el siguiente comando para obtener más opciones de uso para el servidor:</span><span class="sxs-lookup"><span data-stu-id="65177-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="65177-123">**stcpserver.exe/?**</span><span class="sxs-lookup"><span data-stu-id="65177-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="65177-124">A continuación, en el equipo A, inicie el cliente TCP ejecutando lo siguiente en un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="65177-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="65177-125">**stcpclient.exe <DN completo-nombre-de-equipo-B>**</span><span class="sxs-lookup"><span data-stu-id="65177-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="65177-126">En este momento, la conexión debe establecerse de forma segura.</span><span class="sxs-lookup"><span data-stu-id="65177-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="65177-127">Ejecute el siguiente comando para obtener más opciones de uso para el cliente:</span><span class="sxs-lookup"><span data-stu-id="65177-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="65177-128">**stcpclient.exe/?**</span><span class="sxs-lookup"><span data-stu-id="65177-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="65177-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65177-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65177-130">Acerca de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="65177-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="65177-131">Aplicación del nivel de aplicación (ALE)</span><span class="sxs-lookup"><span data-stu-id="65177-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="65177-132">Configuración de IPsec</span><span class="sxs-lookup"><span data-stu-id="65177-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="65177-133">Funciones de IPsec</span><span class="sxs-lookup"><span data-stu-id="65177-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="65177-134">Uso de extensiones de socket seguras</span><span class="sxs-lookup"><span data-stu-id="65177-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="65177-135">Interfaz del proveedor de compatibilidad con seguridad (SSPI)</span><span class="sxs-lookup"><span data-stu-id="65177-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="65177-136">Plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="65177-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="65177-137">Funciones de la API de la plataforma de filtrado de Windows</span><span class="sxs-lookup"><span data-stu-id="65177-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="65177-138">Extensiones Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="65177-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
