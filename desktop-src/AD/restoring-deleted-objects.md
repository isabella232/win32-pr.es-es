---
title: Restaurar objetos eliminados
description: Windows Server 2003 incluye 0034; restore Deleted Objects \ 0034; ofrecen.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Restaurando objetos eliminados AD
- Active Directory, usar, restaurar objetos eliminados
- objetos AD, restaurar objetos eliminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104533088"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="5a68a-106">Restaurar objetos eliminados</span><span class="sxs-lookup"><span data-stu-id="5a68a-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="5a68a-107">Windows Server 2003 incluye la característica "restaurar objetos eliminados".</span><span class="sxs-lookup"><span data-stu-id="5a68a-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="5a68a-108">Para habilitar la restauración de objetos eliminados, al menos un controlador de dominio en el dominio debe ejecutarse en Windows Server 2003 o en una versión posterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="5a68a-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="5a68a-109">De forma predeterminada, solo los administradores de dominio pueden restaurar los objetos eliminados, aunque esto se puede delegar a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="5a68a-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="5a68a-110">Se aplican las siguientes limitaciones a la restauración de objetos eliminados:</span><span class="sxs-lookup"><span data-stu-id="5a68a-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="5a68a-111">No se puede restaurar un objeto cuando la duración del objeto de desecho del objeto ha expirado porque cuando la duración de los objetos de desecho ha expirado, el objeto se elimina permanentemente.</span><span class="sxs-lookup"><span data-stu-id="5a68a-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="5a68a-112">Los objetos que existen en la raíz del contexto de nomenclatura, como un dominio o una partición de aplicación, no se pueden restaurar.</span><span class="sxs-lookup"><span data-stu-id="5a68a-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="5a68a-113">Los objetos de esquema no se pueden restaurar.</span><span class="sxs-lookup"><span data-stu-id="5a68a-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="5a68a-114">Los objetos de esquema no deben eliminarse nunca.</span><span class="sxs-lookup"><span data-stu-id="5a68a-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="5a68a-115">Es posible restaurar los contenedores eliminados, pero la restauración de los objetos eliminados que estaban en el contenedor antes de la eliminación es difícil porque la estructura de árbol del contenedor debe reconstruirse manualmente.</span><span class="sxs-lookup"><span data-stu-id="5a68a-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="5a68a-116">Permisos necesarios para restaurar un objeto eliminado</span><span class="sxs-lookup"><span data-stu-id="5a68a-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="5a68a-117">Cuando se elimina un objeto, se conserva el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="5a68a-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="5a68a-118">Aunque el propietario se puede identificar desde el descriptor de seguridad, por motivos de seguridad, solo los administradores de dominio pueden restaurar los objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="5a68a-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="5a68a-119">Los administradores de dominio pueden conceder el permiso para restaurar los objetos de eliminación a otros usuarios y grupos; para ello, se concede al usuario o grupo el derecho de acceso de control "reanimación de marcadores de exclusión".</span><span class="sxs-lookup"><span data-stu-id="5a68a-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="5a68a-120">El derecho de acceso de control "reanimar marcadores de exclusión" se concede en la raíz del contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="5a68a-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="5a68a-121">Solo los usuarios con permiso de acceso de lectura en un objeto y sus atributos pueden leer el objeto y los atributos accesibles una vez eliminado el objeto.</span><span class="sxs-lookup"><span data-stu-id="5a68a-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="5a68a-122">Conceder a un usuario este permiso puede suponer un riesgo para la seguridad porque podría permitir al usuario restaurar un objeto de cuenta que tiene acceso a los recursos a los que el usuario no tendría acceso normalmente.</span><span class="sxs-lookup"><span data-stu-id="5a68a-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="5a68a-123">Al restaurar una cuenta, el usuario adquiere esencialmente el control de esta cuenta, ya que el usuario debe establecer la contraseña inicial en la cuenta cuando se restaure la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5a68a-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="5a68a-124">Para restaurar completamente un objeto eliminado, el usuario debe:</span><span class="sxs-lookup"><span data-stu-id="5a68a-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="5a68a-125">Tener o ser miembro de un grupo que tenga, el derecho de acceso de control "reanimación de marcadores de exclusión".</span><span class="sxs-lookup"><span data-stu-id="5a68a-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="5a68a-126">Tenga acceso de escritura para cada atributo obligatorio que requiere actualización.</span><span class="sxs-lookup"><span data-stu-id="5a68a-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="5a68a-127">Tener acceso de escritura al nombre distintivo relativo (RDN).</span><span class="sxs-lookup"><span data-stu-id="5a68a-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="5a68a-128">Tenga acceso de escritura a cada atributo opcional que deba actualizarse.</span><span class="sxs-lookup"><span data-stu-id="5a68a-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="5a68a-129">Tener derechos de creación secundarios en el contenedor de destino para la clase de objeto del objeto restaurado.</span><span class="sxs-lookup"><span data-stu-id="5a68a-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="5a68a-130">El atributo **IsDeleted** no se comprueba durante la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="5a68a-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="5a68a-131">Ni se comprobará el permiso Delete-Child en el contenedor "objetos eliminados".</span><span class="sxs-lookup"><span data-stu-id="5a68a-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="5a68a-132">Restaurar un objeto eliminado</span><span class="sxs-lookup"><span data-stu-id="5a68a-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="5a68a-133">Para restaurar un objeto eliminado, primero se debe encontrar el objeto en el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="5a68a-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="5a68a-134">Para obtener más información sobre la recuperación de objetos eliminados, vea [recuperar objetos eliminados](retrieving-deleted-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5a68a-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="5a68a-135">Cuando se encuentra el objeto, se deben completar las siguientes operaciones en una única operación LDAP.</span><span class="sxs-lookup"><span data-stu-id="5a68a-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="5a68a-136">Esto requiere el uso de la [**función \_ \_ ext \_ s de LDAP Modify**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con el [**servidor LDAP para mostrar el control \_ \_ \_ \_ OID eliminado**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .</span><span class="sxs-lookup"><span data-stu-id="5a68a-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="5a68a-137">Quite el valor del atributo **IsDeleted** .</span><span class="sxs-lookup"><span data-stu-id="5a68a-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="5a68a-138">El valor del atributo **IsDeleted** debe quitarse y no debe estar establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="5a68a-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="5a68a-139">Reemplace el nombre distintivo del objeto para que se mueva a un contenedor que no sea el contenedor de objetos eliminados.</span><span class="sxs-lookup"><span data-stu-id="5a68a-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="5a68a-140">Puede ser cualquier contenedor que normalmente pueda contener el objeto.</span><span class="sxs-lookup"><span data-stu-id="5a68a-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="5a68a-141">El nombre distintivo del contenedor anterior del objeto se puede encontrar en el atributo **lastKnownParent** del objeto eliminado.</span><span class="sxs-lookup"><span data-stu-id="5a68a-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="5a68a-142">El atributo **lastKnownParent** solo se establece si el objeto se eliminó en un controlador de dominio de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a68a-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="5a68a-143">Por lo tanto, es posible que el contenido del atributo **lastKnownParent** sea inexacto.</span><span class="sxs-lookup"><span data-stu-id="5a68a-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="5a68a-144">Restaure los atributos obligatorios para el objeto que se borró durante la eliminación.</span><span class="sxs-lookup"><span data-stu-id="5a68a-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="5a68a-145">El atributo **objectCategory** también se puede establecer cuando se restaura el objeto, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="5a68a-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="5a68a-146">Si no se especifica ningún valor **objectCategory** , se utiliza el **objectCategory** predeterminado para el objeto **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="5a68a-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="5a68a-147">Una vez restaurado el objeto, se puede obtener acceso a él como estaba antes de eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="5a68a-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="5a68a-148">En este momento, se deben restaurar todos los atributos opcionales que sean importantes.</span><span class="sxs-lookup"><span data-stu-id="5a68a-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="5a68a-149">También se deben restaurar las referencias al objeto desde otros objetos del directorio.</span><span class="sxs-lookup"><span data-stu-id="5a68a-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="5a68a-150">Como medida de seguridad, los objetos de usuario se deshabilitan cuando se restauran.</span><span class="sxs-lookup"><span data-stu-id="5a68a-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="5a68a-151">Los objetos de usuario deben estar habilitados después de restaurar los atributos opcionales para permitir el uso del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="5a68a-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="5a68a-152">Para obtener más información y un ejemplo de código que muestra cómo restaurar un objeto eliminado, vea la siguiente función RestoreDeletedObject.</span><span class="sxs-lookup"><span data-stu-id="5a68a-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="5a68a-153">RestoreDeletedObject</span><span class="sxs-lookup"><span data-stu-id="5a68a-153">RestoreDeletedObject</span></span>

<span data-ttu-id="5a68a-154">En el ejemplo de código de C++ siguiente se muestra cómo restaurar un objeto eliminado.</span><span class="sxs-lookup"><span data-stu-id="5a68a-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 