---
description: Contiene información que se usa para crear un contexto de Tablet PC.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Estructura de TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003069"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="e9bee-103">Estructura de configuración de \_ contexto de Tablet \_</span><span class="sxs-lookup"><span data-stu-id="e9bee-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="e9bee-104">Contiene información que se usa para crear un contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e9bee-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9bee-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="e9bee-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9bee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9bee-107">**cPktProps**</span><span class="sxs-lookup"><span data-stu-id="e9bee-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-108">El número de propiedades de un paquete.</span><span class="sxs-lookup"><span data-stu-id="e9bee-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-109">**pguidPktProps**</span><span class="sxs-lookup"><span data-stu-id="e9bee-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-110">Identificadores únicos para las propiedades de paquete.</span><span class="sxs-lookup"><span data-stu-id="e9bee-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-111">**cPktBtns**</span><span class="sxs-lookup"><span data-stu-id="e9bee-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-112">Número de botones.</span><span class="sxs-lookup"><span data-stu-id="e9bee-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-113">**pguidPktBtns**</span><span class="sxs-lookup"><span data-stu-id="e9bee-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-114">Identificadores únicos para los botones.</span><span class="sxs-lookup"><span data-stu-id="e9bee-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-115">**pdwBtnDnMask**</span><span class="sxs-lookup"><span data-stu-id="e9bee-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-116">La máscara del botón hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="e9bee-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-117">**pdwBtnUpMask**</span><span class="sxs-lookup"><span data-stu-id="e9bee-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-118">La máscara del botón arriba.</span><span class="sxs-lookup"><span data-stu-id="e9bee-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-119">**lXMargin**</span><span class="sxs-lookup"><span data-stu-id="e9bee-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-120">Margen de la dirección X.</span><span class="sxs-lookup"><span data-stu-id="e9bee-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="e9bee-121">**lYMargin**</span><span class="sxs-lookup"><span data-stu-id="e9bee-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="e9bee-122">Margen de dirección Y.</span><span class="sxs-lookup"><span data-stu-id="e9bee-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9bee-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9bee-123">Remarks</span></span>

<span data-ttu-id="e9bee-124">Normalmente, una aplicación obtiene los valores predeterminados del [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica los valores para satisfacer sus necesidades y, a continuación, pasa la estructura de configuración modificada al [**método ITablet:: CreateContext**](itablet-createcontext.md).</span><span class="sxs-lookup"><span data-stu-id="e9bee-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="e9bee-125">Esta estructura determina qué eventos obtendrá una aplicación, cómo se procesarán y cómo se entregarán a la aplicación o a Windows.</span><span class="sxs-lookup"><span data-stu-id="e9bee-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="e9bee-126">Las máscaras de botón juntas determinan qué tipos de eventos se procesarán en el contexto.</span><span class="sxs-lookup"><span data-stu-id="e9bee-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bee-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9bee-127">Requirements</span></span>



| <span data-ttu-id="e9bee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bee-128">Requirement</span></span> | <span data-ttu-id="e9bee-129">Value</span><span class="sxs-lookup"><span data-stu-id="e9bee-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e9bee-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9bee-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bee-131">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e9bee-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e9bee-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9bee-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bee-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e9bee-133">None supported</span></span><br/>                                     |



 

 




