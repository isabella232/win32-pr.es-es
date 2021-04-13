---
title: DllSurrogate
description: Permite que los servidores DLL se ejecuten en un proceso suplente. Si se especifica una cadena vacía, se usa el suplente proporcionado por el sistema; de lo contrario, el valor especifica la ruta de acceso del suplente que se va a usar.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Valor del registro DllSurrogate COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421459"
---
# <a name="dllsurrogate"></a><span data-ttu-id="6f6e7-105">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="6f6e7-105">DllSurrogate</span></span>

<span data-ttu-id="6f6e7-106">Permite que los servidores DLL se ejecuten en un proceso suplente.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="6f6e7-107">Si se especifica una cadena vacía, se usa el suplente proporcionado por el sistema; de lo contrario, el valor especifica la ruta de acceso del suplente que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6f6e7-108">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="6f6e7-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="6f6e7-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f6e7-109">Remarks</span></span>

<span data-ttu-id="6f6e7-110">Se trata de un valor de **reg \_ SZ** que especifica que la clase es un archivo DLL que se va a activar en un proceso suplente y el proceso suplente que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="6f6e7-111">Para usar el proceso suplente genérico proporcionado por el sistema, establezca *path* en una cadena vacía o **null**.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="6f6e7-112">Para especificar otro proceso suplente, establezca *ruta de acceso* en la ruta de acceso del suplente.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="6f6e7-113">Como en la especificación de la ruta de acceso de un servidor con la clave [**LocalServer32**](localserver32.md) , no es necesario especificar una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="6f6e7-114">El suplente debe estar escrito para comunicarse correctamente con el servicio DCOM tal y como se describe en [escribir un suplente personalizado](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="6f6e7-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="6f6e7-115">El valor **DllSurrogate** debe estar presente para que se active un servidor dll en un suplente.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="6f6e7-116">La activación hace referencia a una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="6f6e7-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="6f6e7-117">La ejecución de archivos dll en un proceso suplente proporciona las ventajas de una implementación ejecutable, incluido el aislamiento de errores, la capacidad de atender a varios clientes simultáneamente y permitir al servidor proporcionar servicios a clientes remotos en un entorno distribuido.</span><span class="sxs-lookup"><span data-stu-id="6f6e7-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f6e7-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f6e7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f6e7-119">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="6f6e7-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="6f6e7-120">Suplentes DLL</span><span class="sxs-lookup"><span data-stu-id="6f6e7-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="6f6e7-121">**DllSurrogateExecutable**</span><span class="sxs-lookup"><span data-stu-id="6f6e7-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="6f6e7-122">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="6f6e7-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 