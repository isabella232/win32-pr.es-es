---
title: Trabajar con listas de revocación
description: Trabajar con listas de revocación
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- SDK de Windows Media Format, listas de revocación
- Advanced Systems Format (ASF), listas de revocación
- ASF (formato de sistemas avanzados), listas de revocación
- listas de revocación
- Administración de derechos digitales (DRM), listas de revocación
- DRM (administración de derechos digitales), listas de revocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532962"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="f766a-109">Trabajar con listas de revocación</span><span class="sxs-lookup"><span data-stu-id="f766a-109">Working with Revocation Lists</span></span>

<span data-ttu-id="f766a-110">Para responder a las infracciones de seguridad y asegurarse de que las aplicaciones del reproductor que se sabe que están interrumpidas o en peligro no pueden reproducir o usar archivos protegidos, cada licencia que se emite contiene una lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="f766a-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="f766a-111">Una lista de revocación contiene los certificados de aplicación de todas las aplicaciones de reproductor que se sabe que están dañados o están dañados.</span><span class="sxs-lookup"><span data-stu-id="f766a-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="f766a-112">Cuando se recibe una nueva licencia, el componente DRM de la aplicación del reproductor comprueba si hay una lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="f766a-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="f766a-113">Si se encuentra una que es más reciente que la que hay actualmente en el equipo, se almacena la lista más reciente.</span><span class="sxs-lookup"><span data-stu-id="f766a-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="f766a-114">La próxima vez que el consumidor reproduzca un archivo ASF protegido, el componente DRM comparará la aplicación de reproducción con la lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="f766a-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="f766a-115">Si se revoca la aplicación de reproducción, el componente DRM envía un mensaje de error a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f766a-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="f766a-116">Las aplicaciones de reproductor pueden recibir un mensaje de error de revocación en los escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="f766a-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="f766a-117">El mensaje de error se recibe una vez que la aplicación llama al método [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) para un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="f766a-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="f766a-118">Se produce un error en la llamada con el código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocado, que se proporciona a la función de devolución de llamada de **Estado** con el estado de la licencia de adquisición de WMT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f766a-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="f766a-119">Si se omite este código **HRESULT** , se seguirán produciendo errores.</span><span class="sxs-lookup"><span data-stu-id="f766a-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="f766a-120">El mensaje de error se recibe cuando la aplicación crea el lector habilitado para DRM y llama al método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) para un archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="f766a-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="f766a-121">Se produce un error en la llamada con el código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocado, que se proporciona al método de devolución de llamada [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) con \_ estado abierto de WMT.</span><span class="sxs-lookup"><span data-stu-id="f766a-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="f766a-122">Cuando una aplicación de reproducción recibe este mensaje de error, la aplicación debe notificar a los usuarios finales y proporcionar una manera de restaurar la funcionalidad de su reproductor.</span><span class="sxs-lookup"><span data-stu-id="f766a-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="f766a-123">Por ejemplo, la aplicación puede abrir una dirección URL en la que los usuarios finales pueden descargar una actualización de la aplicación en peligro.</span><span class="sxs-lookup"><span data-stu-id="f766a-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="f766a-124">**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="f766a-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f766a-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f766a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f766a-126">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="f766a-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="f766a-127">**Control de eventos de adquisición de licencias**</span><span class="sxs-lookup"><span data-stu-id="f766a-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




