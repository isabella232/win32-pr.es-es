---
title: Mensaje de MCIWNDM_OPEN (VFW. h)
description: El \_ mensaje abierto de MCIWNDM abre un dispositivo MCI y lo asocia a una ventana de MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- Mensaje de MCIWNDM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150171"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="7e388-104">MCIWNDM \_ abrir mensaje</span><span class="sxs-lookup"><span data-stu-id="7e388-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="7e388-105">El **mensaje \_ abierto de MCIWNDM** abre un dispositivo MCI y lo asocia a una ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="7e388-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="7e388-106">En el caso de los dispositivos MCI que usan archivos de datos, esta macro también puede abrir un archivo de datos especificado, asignar un nombre a un nuevo archivo que se va a crear o mostrar un cuadro de diálogo para permitir que el usuario seleccione un archivo para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="7e388-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="7e388-107">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .</span><span class="sxs-lookup"><span data-stu-id="7e388-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="7e388-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e388-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e388-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="7e388-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7e388-110">Marcas asociadas al dispositivo o archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="7e388-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="7e388-111">La \_ nueva marca MCIWNDOPENF especifica que se creará un nuevo archivo con el nombre especificado en **szFile**.</span><span class="sxs-lookup"><span data-stu-id="7e388-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="7e388-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span><span class="sxs-lookup"><span data-stu-id="7e388-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="7e388-113">Puntero a una cadena terminada en null que identifica el nombre de archivo o dispositivo MCI que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="7e388-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="7e388-114">Especifique 1 para este parámetro para mostrar el cuadro de diálogo Abrir.</span><span class="sxs-lookup"><span data-stu-id="7e388-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e388-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e388-115">Return Value</span></span>

<span data-ttu-id="7e388-116">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7e388-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e388-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e388-117">Requirements</span></span>



| <span data-ttu-id="7e388-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e388-118">Requirement</span></span> | <span data-ttu-id="7e388-119">Value</span><span class="sxs-lookup"><span data-stu-id="7e388-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7e388-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e388-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e388-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7e388-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7e388-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e388-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e388-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e388-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7e388-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e388-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e388-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e388-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e388-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e388-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e388-127">**MCIWndOpen**</span><span class="sxs-lookup"><span data-stu-id="7e388-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





