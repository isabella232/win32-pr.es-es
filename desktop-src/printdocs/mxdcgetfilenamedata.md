---
description: La \_ estructura MXDC Get \_ filename \_ Data \_ T contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909581"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="a6258-103">MXDC \_ Get \_ filename \_ Data \_ T estructura</span><span class="sxs-lookup"><span data-stu-id="a6258-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="a6258-104">La estructura **MXDC \_ Get \_ filename \_ Data \_ T** contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del convertidor de documentos XPS de Microsoft (MXDC).</span><span class="sxs-lookup"><span data-stu-id="a6258-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6258-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6258-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="a6258-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6258-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6258-107">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="a6258-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="a6258-108">Tamaño del búfer de salida, **wszData**.</span><span class="sxs-lookup"><span data-stu-id="a6258-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="a6258-109">**wszData**</span><span class="sxs-lookup"><span data-stu-id="a6258-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="a6258-110">La ruta de acceso completa y el nombre de archivo del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a6258-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6258-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6258-111">Remarks</span></span>

<span data-ttu-id="a6258-112">[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) devuelve esta estructura cuando se llama con el escape de [**\_ escape MXDC**](mxdc-escape.md) y la estructura [**MXDC de \_ \_ encabezado \_ de escape de**](mxdcescapeheader.md) que se pasa en el parámetro *lpszInData* tiene su código de **operación** establecido en **MXDCOP \_ Get \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="a6258-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6258-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6258-113">Requirements</span></span>



| <span data-ttu-id="a6258-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6258-114">Requirement</span></span> | <span data-ttu-id="a6258-115">Value</span><span class="sxs-lookup"><span data-stu-id="a6258-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a6258-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6258-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6258-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6258-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6258-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6258-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6258-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6258-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a6258-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6258-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6258-121"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6258-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6258-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6258-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6258-123">Impresión</span><span class="sxs-lookup"><span data-stu-id="a6258-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a6258-124">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="a6258-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="a6258-125">[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a6258-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a6258-126">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="a6258-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="a6258-127">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="a6258-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

