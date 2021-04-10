---
title: Instrucciones de seguridad
description: Es importante mantener al usuario informado sobre los posibles problemas de seguridad.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149508"
---
# <a name="security-guideline"></a><span data-ttu-id="5aa29-103">Instrucciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5aa29-103">Security Guideline</span></span>

<span data-ttu-id="5aa29-104">Es importante mantener al usuario informado sobre los posibles problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5aa29-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="5aa29-105">Notificar al usuario de Security-Related eventos</span><span class="sxs-lookup"><span data-stu-id="5aa29-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="5aa29-106">Notifique siempre al usuario cualquier cambio en la seguridad, si se trata de un error relacionado con la seguridad, como un error en el certificado o un cambio en la seguridad del protocolo subyacente, como el cambio de un sitio HTTPS a un sitio HTTP.</span><span class="sxs-lookup"><span data-stu-id="5aa29-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="5aa29-107">Notificar al usuario de Security-Related errores</span><span class="sxs-lookup"><span data-stu-id="5aa29-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="5aa29-108">Cuando la aplicación recibe un mensaje de error que puede indicar un problema de seguridad, la función **InternetErrorDlg** proporciona una interfaz estándar y familiar para notificar al usuario en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="5aa29-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="5aa29-109">Entre los errores que se encuentran en esta categoría se encuentran:</span><span class="sxs-lookup"><span data-stu-id="5aa29-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="5aa29-110">**ERROR \_ de Internet de \_ http \_ a \_ https \_ en \_ redir**</span><span class="sxs-lookup"><span data-stu-id="5aa29-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="5aa29-111">**ERROR \_ de \_ CA no válida de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="5aa29-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="5aa29-112">**ERROR: la \_ publicación en Internet \_ \_ \_ no es \_ segura**</span><span class="sxs-lookup"><span data-stu-id="5aa29-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="5aa29-113">**errores de certificado de ERROR de \_ Internet \_ s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5aa29-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="5aa29-114">**ERROR \_ de \_ \_ certificado CN de Internet \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="5aa29-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="5aa29-115">**ERROR la \_ fecha de certificado de Internet \_ s \_ \_ \_ no es válida**</span><span class="sxs-lookup"><span data-stu-id="5aa29-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="5aa29-116">Un error al notificar al usuario de errores como estos puede exponer al usuario a diferentes tipos de infracciones de seguridad, incluidos los ataques de suplantación de identidad o la divulgación de información involuntaria.</span><span class="sxs-lookup"><span data-stu-id="5aa29-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="5aa29-117">Notificar al usuario cuando cambie la seguridad de la conexión</span><span class="sxs-lookup"><span data-stu-id="5aa29-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="5aa29-118">Notifique siempre al usuario cuando cambie la seguridad de la conexión, por ejemplo, de HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="5aa29-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="5aa29-119">De lo contrario, a menos que el usuario haya elegido explícitamente no recibir notificaciones de estos cambios, está ocultando los riesgos de la divulgación de información involuntaria.</span><span class="sxs-lookup"><span data-stu-id="5aa29-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="5aa29-120">Entre las funciones que informan de este cambio en la seguridad de la conexión se encuentran la función de devolución de llamada **InternetStatusCallback** y la función **InternetConfirmZoneCrossing** .</span><span class="sxs-lookup"><span data-stu-id="5aa29-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="5aa29-121">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="5aa29-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="5aa29-122">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="5aa29-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5aa29-123">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="5aa29-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 