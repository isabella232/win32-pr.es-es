---
description: La estructura PROTOCOLINFO describe un protocolo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Estructura PROTOCOLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678178"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="9ccf0-103">Estructura PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="9ccf0-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="9ccf0-104">La estructura **PROTOCOLINFO** describe un protocolo.</span><span class="sxs-lookup"><span data-stu-id="9ccf0-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ccf0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ccf0-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="9ccf0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ccf0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ccf0-107">**ProtocolID**</span><span class="sxs-lookup"><span data-stu-id="9ccf0-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="9ccf0-108">Identificador de protocolo asignado por el sistema de la sesión de ejecución especificada.</span><span class="sxs-lookup"><span data-stu-id="9ccf0-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="9ccf0-109">**PropertyDatabase**</span><span class="sxs-lookup"><span data-stu-id="9ccf0-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="9ccf0-110">Base de datos de propiedades del protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="9ccf0-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="9ccf0-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="9ccf0-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="9ccf0-112">Nombre abreviado de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9ccf0-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="9ccf0-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="9ccf0-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="9ccf0-114">Nombre de archivo de ayuda opcional asociado al Protocolo.</span><span class="sxs-lookup"><span data-stu-id="9ccf0-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="9ccf0-115">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9ccf0-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="9ccf0-116">Comentario que describe el protocolo.</span><span class="sxs-lookup"><span data-stu-id="9ccf0-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ccf0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ccf0-117">Requirements</span></span>



| <span data-ttu-id="9ccf0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ccf0-118">Requirement</span></span> | <span data-ttu-id="9ccf0-119">Value</span><span class="sxs-lookup"><span data-stu-id="9ccf0-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccf0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ccf0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ccf0-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ccf0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9ccf0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ccf0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ccf0-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ccf0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ccf0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ccf0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ccf0-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ccf0-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




