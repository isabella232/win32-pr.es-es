---
title: Usar StoServe
description: StoServe es un archivo DLL que está diseñado principalmente como un servidor COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665863"
---
# <a name="using-stoserve"></a><span data-ttu-id="0b414-103">Usar StoServe</span><span class="sxs-lookup"><span data-stu-id="0b414-103">Using StoServe</span></span>

<span data-ttu-id="0b414-104">**StoServe** es un archivo DLL que está diseñado principalmente como un servidor com.</span><span class="sxs-lookup"><span data-stu-id="0b414-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="0b414-105">Aunque se puede cargar implícitamente vinculando a su asociado. Archivo LIB, normalmente se utiliza después de una llamada LoadLibrary explícita, normalmente desde dentro de la función COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span><span class="sxs-lookup"><span data-stu-id="0b414-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="0b414-106">**StoServe** es un servidor de proceso de registro automático.</span><span class="sxs-lookup"><span data-stu-id="0b414-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="0b414-107">Para usar **StoServe**, un programa cliente no necesita incluir StoServe. H o vínculo a STOSERVE. Obj.</span><span class="sxs-lookup"><span data-stu-id="0b414-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="0b414-108">Un cliente COM de **StoServe** obtiene el acceso exclusivamente a través de los servicios de CLSID y com de su objeto.</span><span class="sxs-lookup"><span data-stu-id="0b414-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="0b414-109">En el caso de **StoServe**, ese CLSID es CLSID \_ DllPaper (definido en el archivo PAPGUIDS. H en el \\ directorio del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="0b414-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="0b414-110">En el ejemplo de código [StoClien](structured-storage-client-sample--stoclien-.md) se muestra cómo el cliente obtiene este acceso.</span><span class="sxs-lookup"><span data-stu-id="0b414-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="0b414-111">El archivo make que compila este ejemplo registra automáticamente el servidor en el registro.</span><span class="sxs-lookup"><span data-stu-id="0b414-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="0b414-112">Puede iniciar manualmente su propio registro mediante la emisión del comando siguiente en el símbolo del sistema en el directorio **StoServe** :</span><span class="sxs-lookup"><span data-stu-id="0b414-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="0b414-113"> **registro** de NMAKE</span><span class="sxs-lookup"><span data-stu-id="0b414-113">**nmake** **register**</span></span>

<span data-ttu-id="0b414-114">Se supone que tiene un entorno de compilación configurado.</span><span class="sxs-lookup"><span data-stu-id="0b414-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="0b414-115">Si no es así, también puede invocar directamente el comando REGISTER.EXE en el símbolo del sistema mientras se encuentra en el directorio **StoServe**</span><span class="sxs-lookup"><span data-stu-id="0b414-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="0b414-116">**..\\ registrar \\register.exe** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="0b414-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="0b414-117">Estos comandos de registro requieren una compilación anterior del ejemplo de registro en esta serie, así como una compilación anterior de STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="0b414-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="0b414-118">En esta serie, los archivos make usan la utilidad REGISTER.EXE del ejemplo REGISTER.</span><span class="sxs-lookup"><span data-stu-id="0b414-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="0b414-119">Las versiones recientes del kit de desarrollo de software (SDK) de la plataforma y Visual C++ incluyen una utilidad, REGSVR32.EXE, que se puede usar de forma similar para registrar servidores en proceso y calcular las referencias de los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="0b414-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="0b414-120">**StoServe** usa muchas de las clases de utilidad y los servicios proporcionados por apputil.</span><span class="sxs-lookup"><span data-stu-id="0b414-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="0b414-121">Para obtener más detalles sobre APPUTIL, estudie el código fuente de la biblioteca de APPUTIL en el directorio del APPUTIL relacionado y APPUTIL.HTM en el directorio principal del tutorial.</span><span class="sxs-lookup"><span data-stu-id="0b414-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 