---
title: Servicio de datos remotos quitado
description: Los componentes del servidor de servicio de datos remotos se quitan en Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Servidor RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103995697"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="24286-104">Los componentes del servidor de servicio de datos remotos se quitan en Windows 8</span><span class="sxs-lookup"><span data-stu-id="24286-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="24286-105">Plataformas</span><span class="sxs-lookup"><span data-stu-id="24286-105">Platforms</span></span>

 <span data-ttu-id="24286-106">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="24286-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="24286-107">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24286-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="24286-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="24286-108">Description</span></span>

<span data-ttu-id="24286-109">El servidor del servicio de datos remoto (RDS) no está disponible en Windows 8:</span><span class="sxs-lookup"><span data-stu-id="24286-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="24286-110">Se quita el msadcf.dll de archivos, que hospeda el "objeto comercial" predeterminado RDSServer. DataFactory, y se quitan los archivos asociados (msadcfr.dll, msadcfr.dll. MUI, handler. reg y Handsafe. reg)</span><span class="sxs-lookup"><span data-stu-id="24286-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="24286-111">msdfmap.dll de archivo, que es el controlador predeterminado, se quita y se quita el archivo msdfmap.ini</span><span class="sxs-lookup"><span data-stu-id="24286-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="24286-112">msadcs.dll de archivo, ISAPI, se quita</span><span class="sxs-lookup"><span data-stu-id="24286-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="24286-113">Manifestación</span><span class="sxs-lookup"><span data-stu-id="24286-113">Manifestation</span></span>

<span data-ttu-id="24286-114">Los clientes no pueden hospedar un servidor RDS en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="24286-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="24286-115">Mitigación</span><span class="sxs-lookup"><span data-stu-id="24286-115">Mitigation</span></span>

<span data-ttu-id="24286-116">Los clientes pueden mantener su servidor RDS en un equipo con Windows 7 u otros sistemas operativos de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="24286-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="24286-117">Solución</span><span class="sxs-lookup"><span data-stu-id="24286-117">Solution</span></span>

<span data-ttu-id="24286-118">Los clientes pueden mantener su servidor RDS en un equipo con Windows 7 u otros sistemas operativos de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="24286-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="24286-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="24286-119">Resources</span></span>

[<span data-ttu-id="24286-120">Mapa de ruta de las tecnologías de acceso a datos</span><span class="sxs-lookup"><span data-stu-id="24286-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 