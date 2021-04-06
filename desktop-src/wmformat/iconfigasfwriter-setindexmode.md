---
title: IConfigAsfWriter SetIndexMode, método
description: El método SetIndexMode permite que la aplicación controle si el archivo se indizará temporalmente.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Método SetIndexMode formato de Windows Media
- Método SetIndexMode formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077798"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="f845c-106">IConfigAsfWriter:: SetIndexMode (método)</span><span class="sxs-lookup"><span data-stu-id="f845c-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="f845c-107">El método **SetIndexMode** permite que la aplicación controle si el archivo se indizará temporalmente.</span><span class="sxs-lookup"><span data-stu-id="f845c-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f845c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f845c-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="f845c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f845c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f845c-110">*bIndexFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f845c-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f845c-111">Variable de tipo **bool**; **True** especifica que el archivo se indexará temporalmente.</span><span class="sxs-lookup"><span data-stu-id="f845c-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f845c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f845c-112">Return value</span></span>

<span data-ttu-id="f845c-113">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="f845c-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f845c-114">Si se produce un error, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f845c-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f845c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f845c-115">Remarks</span></span>

<span data-ttu-id="f845c-116">De forma predeterminada, el [escritor ASF de WM](wm-asf-writer-filter.md) crea archivos ASF indexados temporalmente.</span><span class="sxs-lookup"><span data-stu-id="f845c-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="f845c-117">Realiza la indexación cuando se detiene el gráfico.</span><span class="sxs-lookup"><span data-stu-id="f845c-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="f845c-118">Puede deshabilitar este comportamiento si desea realizar su propia indexación basada en marco como paso posterior al procesamiento.</span><span class="sxs-lookup"><span data-stu-id="f845c-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="f845c-119">Para crear un archivo indexado por fotogramas, llame a **SetIndexMode**(false), cree el archivo y, a continuación, use los métodos del SDK de Windows Media Format directamente para crear un índice basado en marco para el archivo.</span><span class="sxs-lookup"><span data-stu-id="f845c-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="f845c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f845c-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="f845c-121">[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f845c-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 