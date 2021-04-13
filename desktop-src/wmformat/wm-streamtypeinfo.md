---
title: WM/StreamTypeInfo
description: El atributo WM/StreamTypeInfo contiene la información de configuración para la secuencia especificada en el archivo ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato de Windows Media WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419454"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="f1e9a-104">WM/StreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="f1e9a-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="f1e9a-105">El atributo **WM/StreamTypeInfo** contiene la información de configuración para la secuencia especificada en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f1e9a-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f1e9a-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="f1e9a-106">Global Constant</span></span>

<span data-ttu-id="f1e9a-107">g \_ wszWMStreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="f1e9a-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="f1e9a-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f1e9a-108">Data Type</span></span>

<span data-ttu-id="f1e9a-109">[**WM \_ \_ \_ información de tipo de secuencia**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**tipo WMT \_ \_ binario**)</span><span class="sxs-lookup"><span data-stu-id="f1e9a-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e9a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1e9a-110">Remarks</span></span>

<span data-ttu-id="f1e9a-111">Este atributo se aplica a flujos específicos.</span><span class="sxs-lookup"><span data-stu-id="f1e9a-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="f1e9a-112">No se puede recuperar este atributo para el flujo 0.</span><span class="sxs-lookup"><span data-stu-id="f1e9a-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="f1e9a-113">Este atributo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1e9a-113">This attribute is read-only.</span></span>

<span data-ttu-id="f1e9a-114">El objeto del editor de metadatos puede tener acceso a **WM/StreamTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="f1e9a-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="f1e9a-115">Esta es la única manera de tener acceso a la información de configuración de la secuencia sin abrir el archivo con el objeto lector (o el objeto lector sincrónico).</span><span class="sxs-lookup"><span data-stu-id="f1e9a-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1e9a-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1e9a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e9a-117">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="f1e9a-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




