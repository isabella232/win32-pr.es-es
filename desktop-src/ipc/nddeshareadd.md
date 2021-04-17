---
description: Crea y agrega un nuevo recurso compartido DDE al administrador de bases de datos de recursos compartidos DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Función NDdeShareAdd (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688304"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="9b921-103">NDdeShareAdd función)</span><span class="sxs-lookup"><span data-stu-id="9b921-103">NDdeShareAdd function</span></span>

<span data-ttu-id="9b921-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="9b921-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="9b921-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="9b921-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="9b921-106">Crea y agrega un nuevo recurso compartido DDE al administrador de bases de datos de recursos compartidos DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="9b921-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b921-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b921-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="9b921-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b921-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b921-109">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b921-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b921-110">Nombre del servidor cuyo DSDM se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="9b921-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="9b921-111">*nLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b921-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b921-112">Nivel de información.</span><span class="sxs-lookup"><span data-stu-id="9b921-112">The information level.</span></span> <span data-ttu-id="9b921-113">Este parámetro debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="9b921-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="9b921-114">*pSD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b921-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b921-115">Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que se va a asociar a este recurso compartido y en la que se realizarán las comprobaciones de acceso en los inicios posteriores a este recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="9b921-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="9b921-116">Este parámetro puede ser **null**, en cuyo caso el DSDM crea un descriptor de seguridad predeterminado que concede "control total" al propietario y "lectura y vinculación" a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9b921-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="9b921-117">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9b921-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b921-118">Puntero a la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) que define la lista ApplicationTopic asociada al recurso compartido DDE que se está creando, así como otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b921-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="9b921-119">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9b921-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9b921-120">*cBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b921-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b921-121">Tamaño de la estructura *lpBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="9b921-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="9b921-122">Este parámetro no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="9b921-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b921-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b921-123">Return value</span></span>

<span data-ttu-id="9b921-124">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="9b921-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="9b921-125">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="9b921-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b921-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b921-126">Remarks</span></span>

<span data-ttu-id="9b921-127">Para que un cliente pueda conectarse al recurso compartido DDE, debe ser de confianza con [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span><span class="sxs-lookup"><span data-stu-id="9b921-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b921-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b921-128">Requirements</span></span>



| <span data-ttu-id="9b921-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b921-129">Requirement</span></span> | <span data-ttu-id="9b921-130">Value</span><span class="sxs-lookup"><span data-stu-id="9b921-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b921-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b921-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9b921-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9b921-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9b921-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b921-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9b921-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b921-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9b921-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b921-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b921-136"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b921-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b921-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b921-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b921-138"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b921-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b921-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b921-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b921-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b921-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b921-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="9b921-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9b921-142">**NDdeShareAddW** (Unicode) y **NDdeShareAddA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9b921-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="9b921-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b921-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b921-144">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="9b921-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="9b921-145">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="9b921-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="9b921-146">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="9b921-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="9b921-147">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="9b921-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

