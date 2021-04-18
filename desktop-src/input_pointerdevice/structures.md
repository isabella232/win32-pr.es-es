---
description: En los temas de esta sección se proporcionan las especificaciones de referencia para las estructuras de pila de entrada de dispositivo de puntero.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Estructuras (entrada de dispositivo de puntero)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721647"
---
# <a name="pointer-device-input-stack-structures"></a><span data-ttu-id="51645-103">Estructuras de pila de entrada de dispositivo de puntero</span><span class="sxs-lookup"><span data-stu-id="51645-103">Pointer Device Input Stack structures</span></span>

<span data-ttu-id="51645-104">En los temas de esta sección se proporcionan las especificaciones de referencia para las estructuras de [pila de entrada de dispositivo de puntero](pointer-device-stack-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="51645-104">The topics in this section provide the reference specifications for [Pointer Device Input Stack](pointer-device-stack-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51645-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="51645-105">In this section</span></span>

| <span data-ttu-id="51645-106">Tema</span><span class="sxs-lookup"><span data-stu-id="51645-106">Topic</span></span> | <span data-ttu-id="51645-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="51645-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="51645-108">**POINTER_DEVICE_CURSOR_INFO**</span><span class="sxs-lookup"><span data-stu-id="51645-108">**POINTER_DEVICE_CURSOR_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | <span data-ttu-id="51645-109">Contiene asignaciones de ID. de cursor para dispositivos de puntero.</span><span class="sxs-lookup"><span data-stu-id="51645-109">Contains cursor ID mappings for pointer devices.</span></span><br/> |
| [<span data-ttu-id="51645-110">**POINTER_DEVICE_INFO**</span><span class="sxs-lookup"><span data-stu-id="51645-110">**POINTER_DEVICE_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | <span data-ttu-id="51645-111">Contiene información sobre un dispositivo de puntero.</span><span class="sxs-lookup"><span data-stu-id="51645-111">Contains information about a pointer device.</span></span> <span data-ttu-id="51645-112">Una matriz de estas estructuras se devuelve desde la función [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) .</span><span class="sxs-lookup"><span data-stu-id="51645-112">An array of these structures is returned from the [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) function.</span></span> <span data-ttu-id="51645-113">Una llamada a la función [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) devuelve una única estructura.</span><span class="sxs-lookup"><span data-stu-id="51645-113">A single structure is returned from a call to the [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) function.</span></span> <br/> |
| [<span data-ttu-id="51645-114">**POINTER_DEVICE_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="51645-114">**POINTER_DEVICE_PROPERTY**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | <span data-ttu-id="51645-115">Contiene elementos globales de las propiedades del dispositivo (Dispositivo de interfaz humana (HID) que corresponden a los usos de HID).</span><span class="sxs-lookup"><span data-stu-id="51645-115">Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="51645-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51645-116">Related topics</span></span>

[<span data-ttu-id="51645-117">Referencia de la pila de entrada de dispositivo de puntero</span><span class="sxs-lookup"><span data-stu-id="51645-117">Pointer Device Input Stack Reference</span></span>](unified-input-stack-reference.md)
