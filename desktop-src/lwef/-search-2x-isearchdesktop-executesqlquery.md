---
title: ISearchDesktop ExecuteSQLQuery, método
description: Toma un puntero a una cadena que contiene una consulta de Lenguaje de consulta estructurado (SQL) y sus atributos y devuelve un puntero al conjunto de valores devueltos.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Método ExecuteSQLQuery características del entorno heredado de Windows
- Método ExecuteSQLQuery características de entorno heredado de Windows, interfaz ISearchDesktop
- Interfaz ISearchDesktop características del entorno heredado de Windows, método ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789154"
---
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="18cae-106">ISearchDesktop:: ExecuteSQLQuery (método)</span><span class="sxs-lookup"><span data-stu-id="18cae-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="18cae-107">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18cae-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="18cae-108">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="18cae-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="18cae-109">Toma un puntero a una cadena que contiene una consulta de Lenguaje de consulta estructurado (SQL) y sus atributos y devuelve un puntero al conjunto de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="18cae-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="18cae-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18cae-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="18cae-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18cae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18cae-112">*pdwAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18cae-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cae-113">Tipo: **LPCWSTR \***</span><span class="sxs-lookup"><span data-stu-id="18cae-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="18cae-114">Cadena que contiene los demás atributos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="18cae-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="18cae-115">*pwszURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18cae-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18cae-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="18cae-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="18cae-117">Cadena que contiene la consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="18cae-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="18cae-118">*ppidUrl* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18cae-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18cae-119">Tipo: **ppidUrl \***</span><span class="sxs-lookup"><span data-stu-id="18cae-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="18cae-120">Cuando este método se devuelve correctamente, contiene un puntero al conjunto de registros devuelto.</span><span class="sxs-lookup"><span data-stu-id="18cae-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18cae-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18cae-121">Return value</span></span>

<span data-ttu-id="18cae-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="18cae-122">Type: **HRESULT**</span></span>

<span data-ttu-id="18cae-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="18cae-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18cae-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18cae-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




