---
description: Determina si una aplicación y una cadena de tema (&\# 0034; AppName \| TopicName&\# 0034;) usa la sintaxis correcta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Función NDdeIsValidAppTopicList (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688393"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="9a6eb-103">NDdeIsValidAppTopicList función)</span><span class="sxs-lookup"><span data-stu-id="9a6eb-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="9a6eb-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="9a6eb-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="9a6eb-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="9a6eb-106">Determina si una aplicación y una cadena de tema ("*appname* \| *TopicName*") utiliza la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6eb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a6eb-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="9a6eb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a6eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a6eb-109">*targetTopic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a6eb-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a6eb-110">Un puntero a la aplicación y la cadena de tema que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="9a6eb-111">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a6eb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a6eb-112">Return value</span></span>

<span data-ttu-id="9a6eb-113">Si el parámetro *targetTopic* tiene una sintaxis válida, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="9a6eb-114">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a6eb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a6eb-115">Remarks</span></span>

<span data-ttu-id="9a6eb-116">[**NDdeShareAdd**](nddeshareadd.md) también llama a esta función cuando crea el recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a6eb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a6eb-117">Requirements</span></span>



| <span data-ttu-id="9a6eb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a6eb-118">Requirement</span></span> | <span data-ttu-id="9a6eb-119">Value</span><span class="sxs-lookup"><span data-stu-id="9a6eb-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6eb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a6eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9a6eb-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9a6eb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9a6eb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a6eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9a6eb-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a6eb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9a6eb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a6eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a6eb-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a6eb-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="9a6eb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a6eb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a6eb-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a6eb-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="9a6eb-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a6eb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a6eb-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a6eb-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="9a6eb-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="9a6eb-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9a6eb-131">**NDdeIsValidAppTopicListW** (Unicode) y **NDdeIsValidAppTopicListA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9a6eb-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a6eb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a6eb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a6eb-133">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="9a6eb-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="9a6eb-134">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="9a6eb-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="9a6eb-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="9a6eb-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




