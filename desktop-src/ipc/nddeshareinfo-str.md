---
description: Contiene atributos de recursos compartidos DDE mantenidos por el administrador de bases de datos de recursos compartidos (DSDM)
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Estructura NDDESHAREINFO (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707017"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="c3d57-103">Estructura NDDESHAREINFO</span><span class="sxs-lookup"><span data-stu-id="c3d57-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="c3d57-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="c3d57-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="c3d57-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="c3d57-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="c3d57-106">Contiene atributos de recursos compartidos DDE mantenidos por el administrador de bases de datos de recursos compartidos (DSDM)</span><span class="sxs-lookup"><span data-stu-id="c3d57-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="c3d57-107">El descriptor de seguridad asociado a cada recurso compartido DDE no se pasa a través de esta estructura, pero se obtiene acceso a ella a través de funciones específicas.</span><span class="sxs-lookup"><span data-stu-id="c3d57-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="c3d57-108">La API del DSDM de NetDDE acepta esta estructura para las funciones set. en el caso de las funciones Get, el DSDM devuelve la estructura empaquetada en el búfer suministrado junto con los datos a los que hacen referencia los miembros **lpszShareName**, **lpszAppTopicList** y **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="c3d57-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d57-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3d57-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="c3d57-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3d57-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3d57-111">**lRevision**</span><span class="sxs-lookup"><span data-stu-id="c3d57-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-112">El nivel de revisión de la estructura **NDDESHAREINFO** .</span><span class="sxs-lookup"><span data-stu-id="c3d57-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="c3d57-113">Actualmente, el nivel de revisión es 1.</span><span class="sxs-lookup"><span data-stu-id="c3d57-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-114">**lpszShareName**</span><span class="sxs-lookup"><span data-stu-id="c3d57-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-115">Nombre del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="c3d57-115">The name of the share.</span></span> <span data-ttu-id="c3d57-116">Esta cadena no debe tener más de \_ NDDESHARENAME caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="c3d57-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-117">**lShareType**</span><span class="sxs-lookup"><span data-stu-id="c3d57-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-118">Uno o más tipos de recursos compartidos DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-118">One or more DDE share types.</span></span> <span data-ttu-id="c3d57-119">Este miembro puede ser una combinación de los siguientes tipos de recursos compartidos DDE admitidos.</span><span class="sxs-lookup"><span data-stu-id="c3d57-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="c3d57-120">Tipo de recurso compartido</span><span class="sxs-lookup"><span data-stu-id="c3d57-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="c3d57-121">Significado</span><span class="sxs-lookup"><span data-stu-id="c3d57-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="c3d57-122"><dt>**Recurso compartido \_ Escriba \_ nuevo**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="c3d57-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="c3d57-123">El recurso compartido contiene un par aplicación/tema de OLE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="c3d57-124"><dt>**Recurso compartido \_ Escriba \_ Old**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="c3d57-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="c3d57-125">El recurso compartido contiene un par aplicación/tema de DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="c3d57-126"><dt>**Recurso compartido \_ Escriba \_ static**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="c3d57-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="c3d57-127">El recurso compartido contiene un par aplicación/tema estático.</span><span class="sxs-lookup"><span data-stu-id="c3d57-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3d57-128">**lpszAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="c3d57-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-129">Un puntero a un búfer que contiene cadenas terminadas en null para los pares de aplicación/tema estáticos y de DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="c3d57-130">El búfer debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="c3d57-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="c3d57-131">**fSharedFlag**</span><span class="sxs-lookup"><span data-stu-id="c3d57-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-132">Si este miembro es **false**, el recurso compartido DDE no permitirá que los usuarios remotos se comuniquen mediante el uso de DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="c3d57-133">Sin embargo, los usuarios locales pueden seguir comunicándose a través del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="c3d57-134">Los vínculos de cliente local siempre están implícitos si la DACL asociada concede acceso.</span><span class="sxs-lookup"><span data-stu-id="c3d57-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-135">**fService**</span><span class="sxs-lookup"><span data-stu-id="c3d57-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-136">Si se establece este miembro, el recurso compartido DDE no comprobará si el usuario actual lo ha establecido como de confianza antes de permitir la comunicación DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-137">**fStartAppFlag**</span><span class="sxs-lookup"><span data-stu-id="c3d57-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-138">Si este miembro está establecido y el recurso compartido es de confianza para iniciar aplicaciones, NetDDE intentará iniciar la aplicación especificada por **lpszAppTopicList** si no puede iniciar inicialmente una conversación DDE con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3d57-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-139">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="c3d57-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-140">Cuando NetDDE inicia una aplicación para iniciar una conversación DDE, este valor se envía a la aplicación a través del parámetro *nCmdShow* de la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="c3d57-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="c3d57-141">Define el modo preferido de la ventana de la aplicación que se va a mostrar en.</span><span class="sxs-lookup"><span data-stu-id="c3d57-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="c3d57-142">Este parámetro solo es significativo si **fStartAppFlag** está activo.</span><span class="sxs-lookup"><span data-stu-id="c3d57-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="c3d57-143">El usuario que ha iniciado sesión en cuyo contexto se inicia la aplicación también puede invalidar esta opción al promover el recurso compartido a estado de confianza.</span><span class="sxs-lookup"><span data-stu-id="c3d57-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="c3d57-144">El valor predeterminado para este miembro es SW \_ SHOWMAXIMIZED.</span><span class="sxs-lookup"><span data-stu-id="c3d57-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-145">**qModifyId**</span><span class="sxs-lookup"><span data-stu-id="c3d57-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-146">Número de serie de 8 bytes que indica el número de serie de modificación del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="c3d57-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="c3d57-147">Cada vez que el recurso compartido DDE se modifica mediante una llamada a [**NDdeShareSetInfo**](nddesharesetinfo.md) o [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , se cambian estos valores.</span><span class="sxs-lookup"><span data-stu-id="c3d57-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-148">**cNumItems**</span><span class="sxs-lookup"><span data-stu-id="c3d57-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-149">El número de elementos enumerados en **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="c3d57-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="c3d57-150">Si **cNumItems** es cero, **lpszItemList** está vacío y la información del recurso compartido y el descriptor de seguridad asociado se aplican a todos los elementos a los que presta servicio la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="c3d57-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="c3d57-151">**lpszItemList**</span><span class="sxs-lookup"><span data-stu-id="c3d57-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="c3d57-152">Un puntero a un búfer que contiene cadenas terminadas en null que especifican los elementos en los que la aplicación cliente de una transacción DDE puede solicitar o iniciar bucles de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="c3d57-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="c3d57-153">Si no hay ningún elemento en la lista, el recurso compartido DDE permite el uso de cualquier elemento.</span><span class="sxs-lookup"><span data-stu-id="c3d57-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="c3d57-154">El número de elementos de la lista debe coincidir con el recuento de **cNumItems** .</span><span class="sxs-lookup"><span data-stu-id="c3d57-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3d57-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d57-155">Requirements</span></span>



| <span data-ttu-id="c3d57-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d57-156">Requirement</span></span> | <span data-ttu-id="c3d57-157">Value</span><span class="sxs-lookup"><span data-stu-id="c3d57-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d57-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3d57-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d57-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c3d57-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c3d57-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3d57-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d57-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3d57-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c3d57-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3d57-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3d57-163"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d57-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d57-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3d57-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d57-165">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="c3d57-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="c3d57-166">Estructuras DDE de red</span><span class="sxs-lookup"><span data-stu-id="c3d57-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="c3d57-167">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="c3d57-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="c3d57-168">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="c3d57-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="c3d57-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="c3d57-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

