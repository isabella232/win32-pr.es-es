---
title: Enumeración TYPEMODE (Softkbdc. h)
description: Los elementos de la enumeración TYPEMODE se usan para especificar los modos de tipo que están disponibles para un teclado en pantalla.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- TYPEMODE Enumeration Text Services Framework
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676653"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="5b816-104">Enumeración TYPEMODE</span><span class="sxs-lookup"><span data-stu-id="5b816-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="5b816-105">Los elementos de la enumeración **TYPEMODE** se usan para especificar los modos de tipo que están disponibles para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="5b816-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b816-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b816-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="5b816-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="5b816-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b816-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span><span class="sxs-lookup"><span data-stu-id="5b816-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="5b816-109">El usuario puede hacer clic en las teclas en pantalla para escribir texto.</span><span class="sxs-lookup"><span data-stu-id="5b816-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="5b816-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Activada**</span><span class="sxs-lookup"><span data-stu-id="5b816-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="5b816-111">El usuario puede apuntar a una clave durante un período de tiempo predefinido, y el carácter seleccionado se escribe automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5b816-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="5b816-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Explora**</span><span class="sxs-lookup"><span data-stu-id="5b816-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="5b816-113">El teclado en pantalla examina continuamente el área de entrada y resalta las regiones en las que el usuario puede presionar una tecla de método abreviado o usar un dispositivo de entrada de conmutador.</span><span class="sxs-lookup"><span data-stu-id="5b816-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b816-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b816-114">Requirements</span></span>



| <span data-ttu-id="5b816-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b816-115">Requirement</span></span> | <span data-ttu-id="5b816-116">Value</span><span class="sxs-lookup"><span data-stu-id="5b816-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b816-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b816-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5b816-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b816-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5b816-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b816-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5b816-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b816-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5b816-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5b816-121">Redistributable</span></span><br/>          | <span data-ttu-id="5b816-122">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b816-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="5b816-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b816-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b816-124"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b816-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="5b816-125">IDL</span><span class="sxs-lookup"><span data-stu-id="5b816-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b816-126"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b816-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





