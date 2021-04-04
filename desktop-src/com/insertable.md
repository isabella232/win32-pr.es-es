---
title: Insertable (clave CLSID)
description: Indica que los objetos de esta clase deben aparecer en el cuadro de lista del cuadro de diálogo Insertar objeto cuando lo usan las aplicaciones de contenedor COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- COM de clave del registro insertable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078758"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="eeef0-104">Insertable (clave CLSID)</span><span class="sxs-lookup"><span data-stu-id="eeef0-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="eeef0-105">Indica que los objetos de esta clase deben aparecer en el cuadro de lista del cuadro de diálogo **Insertar objeto** cuando lo usan las aplicaciones de contenedor com.</span><span class="sxs-lookup"><span data-stu-id="eeef0-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="eeef0-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="eeef0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="eeef0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeef0-107">Remarks</span></span>

<span data-ttu-id="eeef0-108">Esta clave es una entrada necesaria para las aplicaciones COM de 32 bits cuyos objetos se pueden insertar en las aplicaciones de 16 bits existentes.</span><span class="sxs-lookup"><span data-stu-id="eeef0-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="eeef0-109">Las aplicaciones de 16 bits existentes buscan esta clave en el registro, lo que informa a la aplicación de que el servidor admite la incrustación.</span><span class="sxs-lookup"><span data-stu-id="eeef0-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="eeef0-110">Si la clave **insertable** existe, las aplicaciones de 16 bits también pueden intentar comprobar que el servidor existe en el equipo.</span><span class="sxs-lookup"><span data-stu-id="eeef0-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="eeef0-111">las aplicaciones de 16 bits normalmente recuperan el valor de la clave [**LocalServer**](localserver.md) de la clase y comprueban si es un archivo válido en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eeef0-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="eeef0-112">Por lo tanto, para que una aplicación de 16 bits pueda insertar una aplicación de 32 bits, la aplicación de 32 bits debe registrar la subclave **LocalServer** además de registrar [**LocalServer32**](localserver32.md).</span><span class="sxs-lookup"><span data-stu-id="eeef0-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="eeef0-113">Cuando se usa con controles, esta entrada indica que un objeto solo puede actuar como un objeto incrustado en contexto sin características de control especiales.</span><span class="sxs-lookup"><span data-stu-id="eeef0-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="eeef0-114">Los objetos que tienen esta clave aparecen en el cuadro de diálogo **Insertar objeto** para su contenedor.</span><span class="sxs-lookup"><span data-stu-id="eeef0-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="eeef0-115">Cuando se usa con controles, esta entrada también indica que el control se ha probado con contenedores que no son de control.</span><span class="sxs-lookup"><span data-stu-id="eeef0-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="eeef0-116">Esta entrada también es opcional y se puede omitir cuando un control no está diseñado para trabajar con contenedores más antiguos que no entienden los controles.</span><span class="sxs-lookup"><span data-stu-id="eeef0-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="eeef0-117">Esta clave no está presente para las clases internas como las clases moniker.</span><span class="sxs-lookup"><span data-stu-id="eeef0-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eeef0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eeef0-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




