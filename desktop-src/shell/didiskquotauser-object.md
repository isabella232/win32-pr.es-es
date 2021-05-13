---
description: Permite a un cliente administrar la configuración de cuota global de disco de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la interfaz DIDiskQuotaUser esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.
title: DiDiskQuotaUser, objeto
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
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843246"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="d7a84-104">DiDiskQuotaUser, objeto</span><span class="sxs-lookup"><span data-stu-id="d7a84-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="d7a84-105">Permite a un cliente administrar la configuración de cuota global de disco de un volumen NTFS.</span><span class="sxs-lookup"><span data-stu-id="d7a84-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="d7a84-106">Este objeto hace que la funcionalidad esencial de la **interfaz DIDiskQuotaUser** esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d7a84-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="d7a84-107">Members</span><span class="sxs-lookup"><span data-stu-id="d7a84-107">Members</span></span>

<span data-ttu-id="d7a84-108">El **objeto DIDiskQuotaUser** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d7a84-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="d7a84-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7a84-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7a84-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7a84-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d7a84-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7a84-111">Methods</span></span>

<span data-ttu-id="d7a84-112">El **objeto DIDiskQuotaUser** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d7a84-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="d7a84-113">Método</span><span class="sxs-lookup"><span data-stu-id="d7a84-113">Method</span></span>                                           | <span data-ttu-id="d7a84-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7a84-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="d7a84-115">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="d7a84-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="d7a84-116">Borra la información de usuario almacenada en caché del objeto.</span><span class="sxs-lookup"><span data-stu-id="d7a84-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d7a84-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7a84-117">Properties</span></span>

<span data-ttu-id="d7a84-118">El **objeto DIDiskQuotaUser** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d7a84-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="d7a84-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7a84-119">Property</span></span>                                                                        | <span data-ttu-id="d7a84-120">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d7a84-120">Access type</span></span>           | <span data-ttu-id="d7a84-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7a84-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7a84-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="d7a84-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="d7a84-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-123">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-124">Obtiene el nombre del contenedor de cuentas del usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="d7a84-125">**AccountStatus**</span><span class="sxs-lookup"><span data-stu-id="d7a84-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="d7a84-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-126">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-127">Obtiene el estado de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="d7a84-128">**Displayname**</span><span class="sxs-lookup"><span data-stu-id="d7a84-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="d7a84-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-129">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-130">Obtiene el nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="d7a84-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="d7a84-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="d7a84-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-132">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-133">Obtiene un identificador que identifica de forma única al usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="d7a84-134">**LogonName**</span><span class="sxs-lookup"><span data-stu-id="d7a84-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="d7a84-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-135">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-136">Obtiene el nombre de la cuenta de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="d7a84-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d7a84-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="d7a84-138">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d7a84-138">Read/write</span></span><br/> | <span data-ttu-id="d7a84-139">Establece u obtiene el límite de cuota [**actual del usuario.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="d7a84-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="d7a84-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="d7a84-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="d7a84-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-141">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-142">Obtiene el límite de cuota actual [**del usuario**](diskquotacontrol-object.md) como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d7a84-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="d7a84-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="d7a84-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="d7a84-144">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="d7a84-144">Read/write</span></span><br/> | <span data-ttu-id="d7a84-145">Establece u obtiene el umbral de advertencia del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d7a84-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="d7a84-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="d7a84-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="d7a84-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-147">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-148">Obtiene el umbral de advertencia del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d7a84-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="d7a84-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="d7a84-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="d7a84-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-150">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-151">Obtiene el uso actual del disco del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d7a84-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="d7a84-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="d7a84-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="d7a84-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7a84-153">Read-only</span></span><br/>  | <span data-ttu-id="d7a84-154">Obtiene el uso actual del disco del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d7a84-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="d7a84-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7a84-155">Remarks</span></span>

<span data-ttu-id="d7a84-156">Cada usuario del volumen administrado por el objeto [**DiskQuotaControl**](diskquotacontrol-object.md) tiene asociado un **objeto DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="d7a84-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="d7a84-157">Este objeto permite a un cliente administrar la configuración de un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="d7a84-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="d7a84-158">Hay varias maneras de obtener el objeto **DIDiskQuotaUser** de un usuario:</span><span class="sxs-lookup"><span data-stu-id="d7a84-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="d7a84-159">Los **objetos DIDiskQuotaUser** para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar.</span><span class="sxs-lookup"><span data-stu-id="d7a84-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="d7a84-160">A continuación se muestra una explicación de **cómo enumerar los objetos DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="d7a84-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="d7a84-161">Al agregar un nuevo usuario, el [**método AddUser**](diskquotacontrol-adduser.md) devuelve el objeto **DIDiskQuotaUser del** usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="d7a84-162">Si tiene el nombre del usuario, el [**método FindUser**](diskquotacontrol-finduser.md) devuelve el objeto **DIDiskQuotaUser del** usuario.</span><span class="sxs-lookup"><span data-stu-id="d7a84-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="d7a84-163">Enumeración de usuarios de cuota de disco</span><span class="sxs-lookup"><span data-stu-id="d7a84-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="d7a84-164">Los **objetos DIDiskQuotaUser** para todos los usuarios con una cuota en el volumen se exponen como una colección.</span><span class="sxs-lookup"><span data-stu-id="d7a84-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="d7a84-165">El [**objeto DiskQuotaControl**](diskquotacontrol-object.md) exporta un método de enumerador estándar que permite enumerar la colección de objetos **DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="d7a84-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="d7a84-166">El procedimiento siguiente muestra cómo realizar la enumeración con Microsoft JScript (compatible con la especificación del lenguaje ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="d7a84-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="d7a84-167">Puede usar un procedimiento similar con Visual Basic o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="d7a84-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="d7a84-168">Cree un nuevo [**objeto DiskQuotaControl.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="d7a84-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="d7a84-169">Inicialíctelo [**con Inicializar**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="d7a84-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="d7a84-170">Cree un nuevo objeto **enumerador de** JScript.</span><span class="sxs-lookup"><span data-stu-id="d7a84-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="d7a84-171">Use un **bucle for** para enumerar los **objetos DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="d7a84-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="d7a84-172">No es necesario establecer un valor inicial.</span><span class="sxs-lookup"><span data-stu-id="d7a84-172">There is no need to set a starting value.</span></span> <span data-ttu-id="d7a84-173">El método **moveNext** del objeto enumerador notifica al método **item** que devuelva el siguiente **objeto DIDiskQuotaUser.**</span><span class="sxs-lookup"><span data-stu-id="d7a84-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="d7a84-174">El **método atEnd** devuelve **false** cuando se llega al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="d7a84-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="d7a84-175">Según sea necesario, use el objeto **DIDiskQuotaUser** devuelto por el método **item** del enumerador para recuperar o establecer una o varias de las propiedades de cuota de disco del usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="d7a84-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="d7a84-176">En el fragmento de código siguiente se muestra cómo enumerar objetos **DIDiskQuotaUser** con JScript.</span><span class="sxs-lookup"><span data-stu-id="d7a84-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="d7a84-177">El **argumento \_ Volume Label** que se pasa a la función **EnumUsers** es un valor de cadena que contiene una etiqueta de volumen como "C: \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="d7a84-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d7a84-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a84-178">Requirements</span></span>



| <span data-ttu-id="d7a84-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a84-179">Requirement</span></span> | <span data-ttu-id="d7a84-180">Value</span><span class="sxs-lookup"><span data-stu-id="d7a84-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a84-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a84-181">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a84-182">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7a84-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7a84-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a84-183">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a84-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7a84-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d7a84-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7a84-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a84-186"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a84-187">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7a84-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a84-188">**Objeto shell**</span><span class="sxs-lookup"><span data-stu-id="d7a84-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




