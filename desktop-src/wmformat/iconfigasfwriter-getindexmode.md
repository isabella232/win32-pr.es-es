---
title: IConfigAsfWriter GetIndexMode, método
description: El método GetIndexMode recupera el modo de índice temporal actual.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Método GetIndexMode formato de Windows Media
- Método GetIndexMode formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420969"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="1178e-106">IConfigAsfWriter:: GetIndexMode (método)</span><span class="sxs-lookup"><span data-stu-id="1178e-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="1178e-107">El método **GetIndexMode** recupera el modo de índice temporal actual.</span><span class="sxs-lookup"><span data-stu-id="1178e-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="1178e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1178e-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="1178e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1178e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1178e-110">*pbIndexFile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1178e-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1178e-111">Puntero a una variable de tipo **bool** que recibe la configuración del modo de índice temporal.</span><span class="sxs-lookup"><span data-stu-id="1178e-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="1178e-112">Un valor de **true** indica que el escritor ASF de WM está configurado para escribir archivos indizados de forma temporal.</span><span class="sxs-lookup"><span data-stu-id="1178e-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1178e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1178e-113">Return value</span></span>

<span data-ttu-id="1178e-114">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="1178e-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="1178e-115">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1178e-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1178e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1178e-116">Remarks</span></span>

<span data-ttu-id="1178e-117">Utilice este método para determinar si el [escritor ASF de WM](wm-asf-writer-filter.md) está configurado actualmente para escribir archivos ASF indexados temporalmente.</span><span class="sxs-lookup"><span data-stu-id="1178e-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="1178e-118">Para obtener más información sobre los archivos indizados y indexados de forma temporal, vea los comentarios de [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md).</span><span class="sxs-lookup"><span data-stu-id="1178e-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1178e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1178e-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="1178e-120">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1178e-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 