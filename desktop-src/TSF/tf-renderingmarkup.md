---
title: Estructura de TF_RENDERINGMARKUP
description: La estructura de la \_ estructura TF RENDERINGMARKUP contiene un intervalo y la información del atributo display.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Marco de TF_RENDERINGMARKUP de servicios de texto de estructura
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685624"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="65f81-104">\_Estructura RENDERINGMARKUP de TF</span><span class="sxs-lookup"><span data-stu-id="65f81-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="65f81-105">La estructura de la estructura [**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contiene un intervalo y la información del atributo display.</span><span class="sxs-lookup"><span data-stu-id="65f81-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f81-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65f81-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="65f81-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="65f81-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="65f81-108">**pRange**</span><span class="sxs-lookup"><span data-stu-id="65f81-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="65f81-109">Puntero a una interfaz [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .</span><span class="sxs-lookup"><span data-stu-id="65f81-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="65f81-110">**tfDisplayAttr**</span><span class="sxs-lookup"><span data-stu-id="65f81-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="65f81-111">Mostrar información de atributos.</span><span class="sxs-lookup"><span data-stu-id="65f81-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65f81-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65f81-112">Remarks</span></span>

<span data-ttu-id="65f81-113">Esta estructura no está actualmente en los archivos de encabezado públicos.</span><span class="sxs-lookup"><span data-stu-id="65f81-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="65f81-114">Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="65f81-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 




