---
title: Enumeración WMDM_FIND_SCOPE
description: El \_ \_ tipo de enumeración de ámbito de búsqueda de WMDM define el ámbito del objeto de almacenamiento.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- Enumeración WMDM_FIND_SCOPE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698697"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="9f568-104">\_Enumeración de ámbito de búsqueda de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="9f568-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="9f568-105">El tipo de enumeración de **\_ \_ ámbito de búsqueda de WMDM** define el ámbito del objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9f568-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f568-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f568-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="9f568-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="9f568-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f568-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**\_ámbito de \_ búsqueda \_ global de WMDM**</span><span class="sxs-lookup"><span data-stu-id="9f568-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="9f568-109">Buscar el objeto coincidente en cualquier parte del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f568-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="9f568-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**\_detectar \_ ámbito de \_ \_ elementos secundarios inmediatos de WMDM**</span><span class="sxs-lookup"><span data-stu-id="9f568-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="9f568-111">Buscar el objeto coincidente dentro de este almacenamiento y sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9f568-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f568-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f568-112">Requirements</span></span>



| <span data-ttu-id="9f568-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f568-113">Requirement</span></span> | <span data-ttu-id="9f568-114">Value</span><span class="sxs-lookup"><span data-stu-id="9f568-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f568-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f568-115">Header</span></span><br/> | <dl> <span data-ttu-id="9f568-116"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f568-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f568-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f568-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f568-118">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="9f568-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





