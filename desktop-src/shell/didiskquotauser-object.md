---
description: Permite a un cliente administrar la configuración de cuota de disco global de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la interfaz DIDiskQuotaUser esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.
title: Objeto DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: 5699ad9d15b0fa31c92f7d88df194f9012fa679d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984275"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="ea0f0-104">Objeto DIDiskQuotaUser</span><span class="sxs-lookup"><span data-stu-id="ea0f0-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="ea0f0-105">Permite a un cliente administrar la configuración de cuota de disco global de un volumen NTFS.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="ea0f0-106">Este objeto hace que la funcionalidad esencial de la interfaz **DIDiskQuotaUser** esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="ea0f0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea0f0-107">Members</span></span>

<span data-ttu-id="ea0f0-108">El objeto **DIDiskQuotaUser** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ea0f0-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="ea0f0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea0f0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea0f0-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea0f0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea0f0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea0f0-111">Methods</span></span>

<span data-ttu-id="ea0f0-112">El objeto **DIDiskQuotaUser** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="ea0f0-113">Método</span><span class="sxs-lookup"><span data-stu-id="ea0f0-113">Method</span></span>                                           | <span data-ttu-id="ea0f0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea0f0-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="ea0f0-115">**Invalidar**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="ea0f0-116">Borra la información de usuario almacenada en caché del objeto.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ea0f0-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea0f0-117">Properties</span></span>

<span data-ttu-id="ea0f0-118">El objeto **DIDiskQuotaUser** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="ea0f0-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea0f0-119">Property</span></span>                                                                        | <span data-ttu-id="ea0f0-120">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="ea0f0-120">Access type</span></span>           | <span data-ttu-id="ea0f0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea0f0-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea0f0-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="ea0f0-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-123">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-124">Obtiene el nombre del contenedor de cuentas del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="ea0f0-125">**Estados**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="ea0f0-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-126">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-127">Obtiene el estado de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="ea0f0-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="ea0f0-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-129">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-130">Obtiene el nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="ea0f0-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="ea0f0-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-132">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-133">Obtiene un identificador que identifica de forma única al usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="ea0f0-134">**LogonName**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="ea0f0-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-135">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-136">Obtiene el nombre de la cuenta de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="ea0f0-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="ea0f0-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-138">Read/write</span></span><br/> | <span data-ttu-id="ea0f0-139">Establece u obtiene el [**límite de cuota**](diskquotacontrol-object.md)actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="ea0f0-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="ea0f0-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-141">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-142">Obtiene el [**límite de cuota**](diskquotacontrol-object.md) actual del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="ea0f0-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="ea0f0-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-144">Read/write</span></span><br/> | <span data-ttu-id="ea0f0-145">Establece u obtiene el umbral de advertencia del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="ea0f0-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="ea0f0-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-147">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-148">Obtiene el umbral de advertencia del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="ea0f0-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="ea0f0-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-150">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-151">Obtiene el uso actual del disco del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="ea0f0-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="ea0f0-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea0f0-153">Read-only</span></span><br/>  | <span data-ttu-id="ea0f0-154">Obtiene el uso actual del disco del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="ea0f0-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea0f0-155">Remarks</span></span>

<span data-ttu-id="ea0f0-156">Cada usuario del volumen administrado por el objeto [**DiskQuotaControl**](diskquotacontrol-object.md) tiene un objeto **DIDiskQuotaUser** asociado a él.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="ea0f0-157">Este objeto permite a un cliente administrar la configuración de un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="ea0f0-158">Hay varias maneras de obtener el objeto **DIDiskQuotaUser** de un usuario:</span><span class="sxs-lookup"><span data-stu-id="ea0f0-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="ea0f0-159">Los objetos **DIDiskQuotaUser** para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="ea0f0-160">A continuación se explica cómo enumerar los objetos **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="ea0f0-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="ea0f0-161">Al agregar un nuevo usuario, el método [**adduser**](diskquotacontrol-adduser.md) devuelve el objeto **DIDiskQuotaUser** del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="ea0f0-162">Si tiene el nombre del usuario, el método [**FindUser**](diskquotacontrol-finduser.md) devuelve el objeto **DIDiskQuotaUser** del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="ea0f0-163">Enumerar usuarios de cuota de disco</span><span class="sxs-lookup"><span data-stu-id="ea0f0-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="ea0f0-164">Los objetos **DIDiskQuotaUser** para todos los usuarios con una cuota en el volumen se exponen como una colección.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="ea0f0-165">El objeto [**DiskQuotaControl**](diskquotacontrol-object.md) exporta un método de enumerador estándar que le permite enumerar la colección de objetos **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="ea0f0-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="ea0f0-166">En el procedimiento siguiente se muestra cómo realizar la enumeración con Microsoft JScript (compatible con la especificación del lenguaje ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="ea0f0-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="ea0f0-167">Puede usar un procedimiento similar con Visual Basic o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="ea0f0-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="ea0f0-168">Cree un nuevo objeto [**DiskQuotaControl**](diskquotacontrol-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ea0f0-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="ea0f0-169">Inicialícelo con [**Initialize**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="ea0f0-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="ea0f0-170">Cree un nuevo objeto de **enumerador** de JScript.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="ea0f0-171">Use un bucle **for** para enumerar los objetos **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="ea0f0-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="ea0f0-172">No es necesario establecer un valor inicial.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-172">There is no need to set a starting value.</span></span> <span data-ttu-id="ea0f0-173">El método **MoveNext** del objeto de enumerador notifica al método **Item** que debe devolver el siguiente objeto **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="ea0f0-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="ea0f0-174">El método **Atend (** devuelve **false** cuando se alcanza el final de la lista.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="ea0f0-175">Según sea necesario, use el objeto **DIDiskQuotaUser** devuelto por el método **Item** del enumerador para recuperar o establecer una o varias propiedades de cuota de disco del usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="ea0f0-176">En el fragmento de código siguiente se muestra cómo enumerar objetos **DIDiskQuotaUser** con JScript.</span><span class="sxs-lookup"><span data-stu-id="ea0f0-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="ea0f0-177">El argumento de la **\_ etiqueta de volumen** que se pasa a la función **EnumUsers** es un valor de cadena que contiene una etiqueta de volumen como "C: \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="ea0f0-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="ea0f0-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea0f0-178">Requirements</span></span>



| <span data-ttu-id="ea0f0-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea0f0-179">Requirement</span></span> | <span data-ttu-id="ea0f0-180">Value</span><span class="sxs-lookup"><span data-stu-id="ea0f0-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0f0-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea0f0-181">Minimum supported client</span></span><br/> | <span data-ttu-id="ea0f0-182">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea0f0-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea0f0-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea0f0-183">Minimum supported server</span></span><br/> | <span data-ttu-id="ea0f0-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea0f0-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ea0f0-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea0f0-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea0f0-186"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f0-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea0f0-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea0f0-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0f0-188">**Objeto de Shell**</span><span class="sxs-lookup"><span data-stu-id="ea0f0-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




