---
description: Notificación enviada al objeto de devolución de llamada de la vista para especificar las ubicaciones y los eventos que se deben registrar para los eventos de notificación de cambios.
title: Mensaje de SFVM_GETNOTIFY (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277638"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="8105f-103">SFVM \_ GETNOTIFY</span><span class="sxs-lookup"><span data-stu-id="8105f-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="8105f-104">Notificación enviada al objeto de devolución de llamada de la vista para especificar las ubicaciones y los eventos que se deben registrar para los eventos de notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="8105f-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="8105f-105">Una vez que se registran, cuando se produce un cambio en en estas ubicaciones o eventos, se notifica el objeto de devolución de llamada de la vista.</span><span class="sxs-lookup"><span data-stu-id="8105f-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="8105f-106">Estos eventos se envían a la devolución de llamada de la vista a través de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) y, a continuación, se controlan mediante la vista.</span><span class="sxs-lookup"><span data-stu-id="8105f-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="8105f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8105f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8105f-108">*PIDL* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8105f-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8105f-109">Un puntero a un IDList absoluto de un elemento para el que la vista debe registrarse para recibir notificaciones de los cambios.</span><span class="sxs-lookup"><span data-stu-id="8105f-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="8105f-110">Normalmente, es el mismo que el IDList de la ubicación que se está viendo, pero puede ser otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="8105f-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8105f-111">La duración de este valor es propiedad del objeto de devolución de llamada de la vista.</span><span class="sxs-lookup"><span data-stu-id="8105f-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="8105f-112">Es responsabilidad del objeto de devolución de llamada de la vista crear y, a continuación, liberar este valor cuando ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="8105f-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="8105f-113">Esto requiere que el objeto de devolución de llamada de la vista almacene este valor.</span><span class="sxs-lookup"><span data-stu-id="8105f-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="8105f-114">Normalmente, el valor se puede almacenar en el miembro **\_ pidlMonitor** del objeto de devolución de llamada de la vista.</span><span class="sxs-lookup"><span data-stu-id="8105f-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="8105f-115">Las reglas de propiedad para el valor devuelto a través de *PIDL* son no estándar y requieren especial atención.</span><span class="sxs-lookup"><span data-stu-id="8105f-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="8105f-116">El objeto de devolución de llamada de vista debe poseer este valor y asegurarse de que no se libera hasta que se destruye el propio objeto de devolución de llamada de la vista.</span><span class="sxs-lookup"><span data-stu-id="8105f-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="8105f-117">*lEvents* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8105f-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8105f-118">Valor que contiene uno o más valores de SHCNE.</span><span class="sxs-lookup"><span data-stu-id="8105f-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="8105f-119">Consulte [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para obtener una lista de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="8105f-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="8105f-120">El objeto de devolución de llamada de vista se registrará para recibir un mensaje de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) cuando se produce cualquiera de los eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="8105f-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8105f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8105f-121">Return value</span></span>

<span data-ttu-id="8105f-122">Se omite, pero debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="8105f-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8105f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8105f-123">Remarks</span></span>

<span data-ttu-id="8105f-124">Si este mensaje de devolución de llamada no devuelve un valor distinto de cero para IDList o la máscara de eventos, la vista no se registrará para las notificaciones de cambio.</span><span class="sxs-lookup"><span data-stu-id="8105f-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="8105f-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8105f-125">Examples</span></span>

<span data-ttu-id="8105f-126">En el ejemplo siguiente se muestra una implementación de ejemplo del código de controlador de la función de devolución de llamada de vista para **SFVM \_ GETNOTIFY**.</span><span class="sxs-lookup"><span data-stu-id="8105f-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="8105f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8105f-127">Requirements</span></span>



| <span data-ttu-id="8105f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8105f-128">Requirement</span></span> | <span data-ttu-id="8105f-129">Value</span><span class="sxs-lookup"><span data-stu-id="8105f-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8105f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8105f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8105f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8105f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8105f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8105f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8105f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8105f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8105f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8105f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8105f-135"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8105f-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8105f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8105f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8105f-137">**SFVM \_ QUERYFSNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="8105f-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="8105f-138">**IShellFolderViewCB::MessageSFVCB**</span><span class="sxs-lookup"><span data-stu-id="8105f-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
