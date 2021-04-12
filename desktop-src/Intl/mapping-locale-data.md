---
description: NLS incluye una serie de funciones de API que las aplicaciones pueden usar para asignar datos de configuración regional entre los identificadores de configuración regional y los nombres de configuración regional, y para enumerar las configuraciones regionales neutras.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Asignar datos de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275764"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="fe0dd-103">Asignar datos de configuración regional</span><span class="sxs-lookup"><span data-stu-id="fe0dd-103">Mapping Locale Data</span></span>

<span data-ttu-id="fe0dd-104">NLS incluye una serie de funciones de API que las aplicaciones pueden usar para asignar datos de configuración regional entre los [identificadores de configuración](locale-identifiers.md) regional y [los nombres de configuración regional](locale-names.md), y para enumerar las configuraciones regionales neutras.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="fe0dd-105">En este tema se describe el uso de estas funciones en Windows Vista y versiones posteriores y en los sistemas operativos anteriores a Windows Vista (a veces denominados "sistemas de nivel inferior").</span><span class="sxs-lookup"><span data-stu-id="fe0dd-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="fe0dd-106">Asignar datos de configuración regional en Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="fe0dd-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="fe0dd-107">NLS proporciona varias funciones de asignación de configuración regional para que las usen las aplicaciones que desarrolle para ejecutarse en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="fe0dd-108">También incluye funciones que las aplicaciones pueden usar para enumerar configuraciones regionales neutras.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="fe0dd-109">**Usar las funciones de conversión estándar para la asignación de datos**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="fe0dd-110">Para asignar entre un nombre de configuración regional y un identificador de configuración regional, la aplicación puede llamar a la función [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) .</span><span class="sxs-lookup"><span data-stu-id="fe0dd-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="fe0dd-111">La aplicación usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para asignar entre un identificador de configuración regional y un nombre de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="fe0dd-112">**Enumerar configuraciones regionales neutras**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-112">**List Neutral Locales**</span></span>

<span data-ttu-id="fe0dd-113">Para enumerar las configuraciones regionales neutras para Windows 7 y versiones posteriores, la aplicación puede llamar a [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) con *dwFlags* establecido en [**\_ NEUTRALDATA de configuración regional**](locale-neutraldata.md).</span><span class="sxs-lookup"><span data-stu-id="fe0dd-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="fe0dd-114">También puede usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* establecido en [**configuración regional \_ INEUTRAL**](locale-ineutral.md).</span><span class="sxs-lookup"><span data-stu-id="fe0dd-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="fe0dd-115">Asignar datos de configuración regional en sistemas operativos anteriores a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe0dd-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="fe0dd-116">NLS incluye una biblioteca de vínculos directos (DLL) que se utiliza para las aplicaciones que se desarrollan para ejecutarse en sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="fe0dd-117">El archivo DLL admite las funciones de conversión y enumeración para la asignación de datos.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="fe0dd-118">Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores no deben usar las funciones de lista o asignación de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="fe0dd-119">**Usar las funciones de conversión de nivel inferior para la asignación de datos**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="fe0dd-120">La aplicación destinada a un sistema de nivel inferior puede llamar a la función [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) para convertir un identificador de configuración regional en un nombre de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="fe0dd-121">Si necesita convertir un nombre de configuración regional en un identificador de configuración regional, debe llamar a [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span><span class="sxs-lookup"><span data-stu-id="fe0dd-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="fe0dd-122">**Usar las funciones de lista de bajo nivel para enumerar configuraciones regionales neutras**</span><span class="sxs-lookup"><span data-stu-id="fe0dd-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="fe0dd-123">La aplicación debe llamar a [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) para recuperar el identificador de configuración regional del elemento primario de una configuración regional.</span><span class="sxs-lookup"><span data-stu-id="fe0dd-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="fe0dd-124">Si la aplicación necesita obtener el nombre de configuración regional del elemento primario para la configuración regional, debe llamar a [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span><span class="sxs-lookup"><span data-stu-id="fe0dd-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe0dd-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe0dd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe0dd-126">Uso de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="fe0dd-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="fe0dd-127">Identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="fe0dd-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="fe0dd-128">Nombres de configuración regional</span><span class="sxs-lookup"><span data-stu-id="fe0dd-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



