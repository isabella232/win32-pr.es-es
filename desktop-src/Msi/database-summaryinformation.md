---
description: La propiedad SummaryInformation del objeto de base de datos devuelve un objeto SummaryInfo que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de información de resumen.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Propiedad Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653982"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="03b53-103">Propiedad Database. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="03b53-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="03b53-104">La propiedad **SummaryInformation** del objeto de [**base de datos**](database-object.md) devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de [información de Resumen](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="03b53-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="03b53-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="03b53-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b53-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03b53-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="03b53-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="03b53-107">Property value</span></span>

<span data-ttu-id="03b53-108">Número máximo de propiedades que se van a agregar o modificar.</span><span class="sxs-lookup"><span data-stu-id="03b53-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="03b53-109">Este parámetro es necesario y se usa para asignar suficiente memoria de trabajo durante la generación del flujo.</span><span class="sxs-lookup"><span data-stu-id="03b53-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="03b53-110">No es necesario almacenar este número de propiedades.</span><span class="sxs-lookup"><span data-stu-id="03b53-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="03b53-111">Se debe utilizar un valor de cero si la base de datos se abre como de solo lectura para evitar que se actualice la secuencia.</span><span class="sxs-lookup"><span data-stu-id="03b53-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="03b53-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03b53-112">Remarks</span></span>

<span data-ttu-id="03b53-113">Si se usa un valor de *maxProperties* mayor que 0 para abrir una secuencia de información de Resumen existente, se debe llamar al método [**Persist**](summaryinfo-persist.md) antes de cerrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="03b53-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="03b53-114">Si no lo hace, perderá la información de la secuencia existente.</span><span class="sxs-lookup"><span data-stu-id="03b53-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="03b53-115">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="03b53-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b53-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03b53-116">Requirements</span></span>



| <span data-ttu-id="03b53-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="03b53-117">Requirement</span></span> | <span data-ttu-id="03b53-118">Value</span><span class="sxs-lookup"><span data-stu-id="03b53-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b53-119">Versión</span><span class="sxs-lookup"><span data-stu-id="03b53-119">Version</span></span><br/> | <span data-ttu-id="03b53-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03b53-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03b53-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03b53-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03b53-122">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="03b53-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="03b53-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03b53-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="03b53-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b53-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="03b53-125">IID</span><span class="sxs-lookup"><span data-stu-id="03b53-125">IID</span></span><br/>     | <span data-ttu-id="03b53-126">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03b53-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




