---
description: Ejemplos de controles parentales
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Ejemplos de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697519"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="297d2-103">Ejemplos de controles parentales</span><span class="sxs-lookup"><span data-stu-id="297d2-103">Parental Controls Samples</span></span>

<span data-ttu-id="297d2-104">El código de ejemplo para controles parentales está disponible en ruta de acceso <installation directory> \\ ejemplos de Windows \\ <version number> \\ \\ seguridad \\ ParentalControls.</span><span class="sxs-lookup"><span data-stu-id="297d2-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="297d2-105">Los ejemplos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="297d2-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="297d2-106">Sectores públicos</span><span class="sxs-lookup"><span data-stu-id="297d2-106">Utilities</span></span>

<span data-ttu-id="297d2-107">Funcionalidad auxiliar para la administración básica de COM, las operaciones de cadenas de SID y la funcionalidad de lectura y escritura de WMI.</span><span class="sxs-lookup"><span data-stu-id="297d2-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="297d2-108">Todos los demás ejemplos dependen de este proyecto, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="297d2-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="297d2-109">ComplianceAPI</span><span class="sxs-lookup"><span data-stu-id="297d2-109">ComplianceAPI</span></span>

<span data-ttu-id="297d2-110">Aplicación de consola controlada por línea de comandos que muestra cómo usar la API de cumplimiento para recuperar un subconjunto clave de la configuración de un usuario.</span><span class="sxs-lookup"><span data-stu-id="297d2-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="297d2-111">ComplianceApp</span><span class="sxs-lookup"><span data-stu-id="297d2-111">ComplianceApp</span></span>

<span data-ttu-id="297d2-112">Aplicación de consola simple que muestra el uso de la API de cumplimiento para comprobar el registro necesario y las restricciones específicas.</span><span class="sxs-lookup"><span data-stu-id="297d2-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="297d2-113">Si se habilitan las restricciones de tiempo, la aplicación también espera los eventos de cierre de sesión inminentes.</span><span class="sxs-lookup"><span data-stu-id="297d2-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="297d2-114">UIExtensibility</span><span class="sxs-lookup"><span data-stu-id="297d2-114">UIExtensibility</span></span>

<span data-ttu-id="297d2-115">Aplicación de consola controlada por línea de comandos en la que se muestra el uso de las API de WMI y el esquema WPC para enumerar, consultar, agregar, modificar y eliminar entradas de vínculo de extensibilidad de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="297d2-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="297d2-116">Ejemplo de línea de comandos para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="297d2-116">Example command line for sample:</span></span>

<span data-ttu-id="297d2-117">"D: \\ WPC \\ Samples \\ Security \\ ParentalControls \\ UIExtensibility \\ Debug \\ UIExtensibility" Add/g: {FD59BB7F-54AB-11DB-9666-00E08161165F}/c: 0/N: D:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-101/S: d:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-103/I: d:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-104/D: d:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="297d2-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="297d2-118">donde UiExtRC es un archivo DLL de recursos simple con recursos de cadena para los IDENTIFICADOres 101 y 103, y 24x24 pixel 32-bit con mapas de bits alfa para los recursos 104 y 106.</span><span class="sxs-lookup"><span data-stu-id="297d2-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="297d2-119">WebExtensibility</span><span class="sxs-lookup"><span data-stu-id="297d2-119">WebExtensibility</span></span>

<span data-ttu-id="297d2-120">Aplicación de consola controlada por línea de comandos que muestra cómo usar las API de WMI y el esquema WPC para enumerar, agregar y eliminar entradas de aplicación HTTP o de exención de URL, y para establecer y restablecer una invalidación de filtro de contenido web con las propiedades FilterID y FilterName.</span><span class="sxs-lookup"><span data-stu-id="297d2-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="297d2-121">No se muestra el acceso a la aplicación HTTP de solo lectura y a las listas de exenciones de URL, pero el código para leer las listas sería el mismo que para el caso de lectura/escritura, excepto para la modificación del parámetro WMI.</span><span class="sxs-lookup"><span data-stu-id="297d2-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



