---
title: Componentes de Windows instalados a petición
description: Componentes de Windows instalados a petición
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078500"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="e1a2c-103">Componentes de Windows instalados a petición</span><span class="sxs-lookup"><span data-stu-id="e1a2c-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="e1a2c-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="e1a2c-104">Platform</span></span>

<span data-ttu-id="e1a2c-105">**Clientes-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e1a2c-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="e1a2c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1a2c-106">Description</span></span>

<span data-ttu-id="e1a2c-107">Dos componentes de Windows se instalarán a petición en Windows 8.1: DirectPlay y NTVDM.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="e1a2c-108">Estos componentes se enumeran en componentes opcionales en el nodo "componentes heredados".</span><span class="sxs-lookup"><span data-stu-id="e1a2c-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="e1a2c-109">Estos componentes se instalan localmente como parte del sistema operativo y se comprimen como componentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="e1a2c-110">Cuando una aplicación hace referencia o llama a uno de estos componentes (normalmente en el primer inicio de la aplicación), la instalación se desencadena automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="e1a2c-111">Los usuarios recibirán una notificación de que el componente se instalará y deben confirmar la acción para poder continuar.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="e1a2c-112">La elevación es necesaria para que esto se realice correctamente si el usuario no es un administrador.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="e1a2c-113">Después de la instalación inicial, el usuario no necesita realizar ninguna otra acción para usar el componente de nuevo.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="e1a2c-114">Manifestación</span><span class="sxs-lookup"><span data-stu-id="e1a2c-114">Manifestation</span></span>

<span data-ttu-id="e1a2c-115">Cuando una aplicación hace referencia o llama a un componente heredado en componentes opcionales (en el primer inicio), se suspenderá la aplicación y se abrirá el cuadro de diálogo de características a petición, que solicitará permiso al usuario para instalar el componente.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="e1a2c-116">Si los usuarios hacen clic en aceptar, también pueden ver una petición de elevación en la que deben escribir sus credenciales.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="e1a2c-117">A continuación, se instalará el componente y se reanudará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="e1a2c-118">Mitigación</span><span class="sxs-lookup"><span data-stu-id="e1a2c-118">Mitigation</span></span>

<span data-ttu-id="e1a2c-119">Para evitar que se abra la interfaz de usuario de características a petición, puede preinstalar DirectPlay y NTVDM mediante DISM o la interfaz de usuario de componentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="e1a2c-120">Solución</span><span class="sxs-lookup"><span data-stu-id="e1a2c-120">Solution</span></span>

<span data-ttu-id="e1a2c-121">Se recomienda encarecidamente evitar la referencia o la llamada a los componentes que se han enumerado como componentes opcionales heredados en Windows en versiones futuras de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="e1a2c-122">Los componentes opcionales heredados incluirán solo los componentes más antiguos y menos usados que podrían causar problemas de rendimiento y seguridad para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="e1a2c-123">Pruebas</span><span class="sxs-lookup"><span data-stu-id="e1a2c-123">Tests</span></span>

<span data-ttu-id="e1a2c-124">No se necesitan alojamientos de prueba adicionales para la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="e1a2c-125">Es importante tener en cuenta que este cuadro de diálogo aparecerá cuando se llame al componente opcional o se haga referencia a él, y esta instalación requiere elevación.</span><span class="sxs-lookup"><span data-stu-id="e1a2c-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




