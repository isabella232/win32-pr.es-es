---
description: La propiedad Environment del objeto Installer es una propiedad de lectura y escritura que es el valor de cadena de una variable de entorno del proceso actual.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer. Environment (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653353"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="c12d8-103">Installer. Environment (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c12d8-103">Installer.Environment property</span></span>

<span data-ttu-id="c12d8-104">La propiedad **Environment** del objeto [**Installer**](installer-object.md) es una propiedad de lectura y escritura que es el valor de cadena de una variable de entorno del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="c12d8-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="c12d8-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c12d8-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c12d8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c12d8-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="c12d8-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c12d8-107">Property value</span></span>

<span data-ttu-id="c12d8-108">Nombre de la variable de entorno que se va a leer o escribir.</span><span class="sxs-lookup"><span data-stu-id="c12d8-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="c12d8-109">No distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c12d8-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="c12d8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c12d8-110">Remarks</span></span>

<span data-ttu-id="c12d8-111">El establecimiento de una variable de entorno con la propiedad de **entorno** solo afecta a la sesión activa.</span><span class="sxs-lookup"><span data-stu-id="c12d8-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="c12d8-112">Para realizar cambios persistentes en una variable de entorno, utilice la [tabla de entorno](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="c12d8-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c12d8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c12d8-113">Requirements</span></span>



| <span data-ttu-id="c12d8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c12d8-114">Requirement</span></span> | <span data-ttu-id="c12d8-115">Value</span><span class="sxs-lookup"><span data-stu-id="c12d8-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12d8-116">Versión</span><span class="sxs-lookup"><span data-stu-id="c12d8-116">Version</span></span><br/> | <span data-ttu-id="c12d8-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c12d8-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c12d8-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c12d8-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c12d8-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c12d8-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c12d8-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c12d8-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c12d8-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c12d8-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c12d8-122">IID</span><span class="sxs-lookup"><span data-stu-id="c12d8-122">IID</span></span><br/>     | <span data-ttu-id="c12d8-123">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c12d8-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




