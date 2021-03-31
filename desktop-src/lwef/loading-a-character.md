---
title: Cargar un carácter
description: Cargar un carácter
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775913"
---
# <a name="loading-a-character"></a><span data-ttu-id="390cb-103">Cargar un carácter</span><span class="sxs-lookup"><span data-stu-id="390cb-103">Loading a Character</span></span>

<span data-ttu-id="390cb-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="390cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="390cb-105">Para animar un carácter, primero debe cargar el carácter.</span><span class="sxs-lookup"><span data-stu-id="390cb-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="390cb-106">Use el método [**Load**](load-method.md) para cargar los datos del carácter.</span><span class="sxs-lookup"><span data-stu-id="390cb-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="390cb-107">El agente de Microsoft admite dos formatos de datos de caracteres y de animación: un único archivo estructurado y archivos independientes.</span><span class="sxs-lookup"><span data-stu-id="390cb-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="390cb-108">Normalmente, se usa el formato de archivo único (. ACS) cuando los datos se almacenan de forma local.</span><span class="sxs-lookup"><span data-stu-id="390cb-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="390cb-109">El formato de varios archivos (. ACF,. ACA) funciona mejor cuando desea descargar animaciones de forma individual, por ejemplo, al tener acceso a animaciones desde un servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="390cb-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="390cb-110">Una aplicación cliente puede cargar una sola instancia del mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="390cb-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="390cb-111">Cualquier intento de cargar el mismo carácter más de una vez producirá un error.</span><span class="sxs-lookup"><span data-stu-id="390cb-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="390cb-112">Sin embargo, una aplicación puede tener varias instancias del mismo carácter cargadas proporcionando conexiones independientes al agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="390cb-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="390cb-113">Por ejemplo, una aplicación podría cargar el mismo carácter de dos copias del control Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="390cb-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="390cb-114">También puede definir sus propios caracteres para su uso con Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="390cb-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="390cb-115">Puede usar cualquier herramienta de representación que prefiera para crear las imágenes, siempre y cuando acabe con los archivos de formato de mapa de bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="390cb-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="390cb-116">Para ensamblar y compilar las imágenes de un carácter en animaciones para su uso con el agente de Microsoft, use el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="390cb-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="390cb-117">Esta herramienta permite definir las propiedades predeterminadas de un carácter, así como definir animaciones para el carácter.</span><span class="sxs-lookup"><span data-stu-id="390cb-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="390cb-118">El editor de caracteres del agente de Microsoft también permite seleccionar el formato de archivo adecuado al crear un carácter.</span><span class="sxs-lookup"><span data-stu-id="390cb-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




