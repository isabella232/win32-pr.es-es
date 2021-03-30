---
description: Representa información sobre una conexión a una impresora.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Estructura de PRINTER_CONNECTION_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814867"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="e639c-103">Estructura de la información de conexión de impresora \_ \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="e639c-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="e639c-104">Representa información sobre una conexión a una impresora.</span><span class="sxs-lookup"><span data-stu-id="e639c-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e639c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e639c-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="e639c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e639c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e639c-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="e639c-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e639c-108">Se definen los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="e639c-108">The following values are defined:</span></span>



| <span data-ttu-id="e639c-109">Value</span><span class="sxs-lookup"><span data-stu-id="e639c-109">Value</span></span>                                      | <span data-ttu-id="e639c-110">Significado</span><span class="sxs-lookup"><span data-stu-id="e639c-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e639c-111">Conexión de impresora \_ \_ no coincidente (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e639c-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="e639c-112">Si se establece esta marca de bits, la conexión de impresora no coincide.</span><span class="sxs-lookup"><span data-stu-id="e639c-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="e639c-113">El usuario puede proporcionar un controlador de impresión local como *pszDriverName* y usarlo para realizar la representación en lugar de usar el controlador instalado en la impresora del servidor a la que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="e639c-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="e639c-114">Conexión de impresora \_ \_ sin \_ interfaz de usuario (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="e639c-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="e639c-115">Si se establece esta marca de bits, esta llamada no puede mostrar un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e639c-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="e639c-116">Si se debe mostrar un cuadro de diálogo para instalar un controlador de impresora desde el servidor y esta marca de bits está establecida, el controlador de impresora no se instalará, la conexión de impresora no se agregará y se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="e639c-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="e639c-117">**Windows 7:** En Windows 7 y versiones posteriores de Windows, si se establece esta marca y el usuario se ejecuta en modo con privilegios elevados, no se mostrará el cuadro de diálogo **¿confía en esta impresora?** .</span><span class="sxs-lookup"><span data-stu-id="e639c-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e639c-118">**pszDriverName**</span><span class="sxs-lookup"><span data-stu-id="e639c-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="e639c-119">Puntero al nombre del controlador.</span><span class="sxs-lookup"><span data-stu-id="e639c-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e639c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e639c-120">Requirements</span></span>



| <span data-ttu-id="e639c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e639c-121">Requirement</span></span> | <span data-ttu-id="e639c-122">Value</span><span class="sxs-lookup"><span data-stu-id="e639c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e639c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e639c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e639c-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e639c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e639c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e639c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e639c-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e639c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e639c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e639c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e639c-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e639c-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e639c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e639c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e639c-130">Impresión</span><span class="sxs-lookup"><span data-stu-id="e639c-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e639c-131">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="e639c-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




