---
description: Especifica un archivo que se va a firmar.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Estructura de SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668480"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="13d0f-103">Estructura de \_ información del archivo del firmante \_</span><span class="sxs-lookup"><span data-stu-id="13d0f-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="13d0f-104">La estructura de **\_ \_ información del archivo del firmante** especifica el archivo que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="13d0f-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="13d0f-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="13d0f-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="13d0f-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="13d0f-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="13d0f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13d0f-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="13d0f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="13d0f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="13d0f-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="13d0f-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="13d0f-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="13d0f-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="13d0f-111">**pwszFileName**</span><span class="sxs-lookup"><span data-stu-id="13d0f-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="13d0f-112">Puntero a una cadena terminada en null que contiene el nombre del archivo que se va a firmar.</span><span class="sxs-lookup"><span data-stu-id="13d0f-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="13d0f-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="13d0f-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="13d0f-114">Identificador abierto del archivo especificado por el miembro **pwszFileName** .</span><span class="sxs-lookup"><span data-stu-id="13d0f-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="13d0f-115">Si este miembro contiene un identificador válido, este identificador se utiliza para obtener acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="13d0f-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="13d0f-116">Este miembro se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="13d0f-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13d0f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d0f-117">Requirements</span></span>



| <span data-ttu-id="13d0f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d0f-118">Requirement</span></span> | <span data-ttu-id="13d0f-119">Value</span><span class="sxs-lookup"><span data-stu-id="13d0f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="13d0f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13d0f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13d0f-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="13d0f-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="13d0f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13d0f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13d0f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="13d0f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13d0f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="13d0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d0f-125">**información de \_ asunto del firmante \_**</span><span class="sxs-lookup"><span data-stu-id="13d0f-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




