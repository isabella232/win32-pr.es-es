---
description: El método commit del objeto de base de datos finaliza el formulario persistente de la base de datos.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653862"
---
# <a name="databasecommit-method"></a><span data-ttu-id="fa782-103">Database. Commit (método)</span><span class="sxs-lookup"><span data-stu-id="fa782-103">Database.Commit method</span></span>

<span data-ttu-id="fa782-104">El método **commit** del objeto de [**base de datos**](database-object.md) finaliza el formulario persistente de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa782-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="fa782-105">Todos los datos persistentes se escriben en la base de datos grabable y no se escriben columnas ni filas temporales.</span><span class="sxs-lookup"><span data-stu-id="fa782-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="fa782-106">Este método no tiene ningún efecto en una base de datos abierta como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fa782-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="fa782-107">Se puede llamar a este método varias veces para guardar el estado actual de las tablas cargadas en la memoria.</span><span class="sxs-lookup"><span data-stu-id="fa782-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="fa782-108">Cuando se cierra la base de datos, se revierten los cambios realizados después de la última **confirmación** .</span><span class="sxs-lookup"><span data-stu-id="fa782-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="fa782-109">Normalmente, se llama a este método antes de cerrarse cuando se han finalizado todos los cambios en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa782-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa782-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa782-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="fa782-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa782-111">Parameters</span></span>

<span data-ttu-id="fa782-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fa782-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa782-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa782-113">Return value</span></span>

<span data-ttu-id="fa782-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fa782-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa782-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa782-115">Remarks</span></span>

<span data-ttu-id="fa782-116">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="fa782-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa782-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa782-117">Requirements</span></span>



| <span data-ttu-id="fa782-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa782-118">Requirement</span></span> | <span data-ttu-id="fa782-119">Value</span><span class="sxs-lookup"><span data-stu-id="fa782-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa782-120">Versión</span><span class="sxs-lookup"><span data-stu-id="fa782-120">Version</span></span><br/> | <span data-ttu-id="fa782-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa782-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fa782-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fa782-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fa782-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa782-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fa782-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa782-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa782-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa782-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fa782-126">IID</span><span class="sxs-lookup"><span data-stu-id="fa782-126">IID</span></span><br/>     | <span data-ttu-id="fa782-127">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fa782-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




