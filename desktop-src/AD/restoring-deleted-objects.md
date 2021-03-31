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
# <a name="restoring-deleted-objects"></a>Restaurar objetos eliminados

Windows Server 2003 incluye la característica "restaurar objetos eliminados".

Para habilitar la restauración de objetos eliminados, al menos un controlador de dominio en el dominio debe ejecutarse en Windows Server 2003 o en una versión posterior de Windows. De forma predeterminada, solo los administradores de dominio pueden restaurar los objetos eliminados, aunque esto se puede delegar a otros usuarios.

Se aplican las siguientes limitaciones a la restauración de objetos eliminados:

-   No se puede restaurar un objeto cuando la duración del objeto de desecho del objeto ha expirado porque cuando la duración de los objetos de desecho ha expirado, el objeto se elimina permanentemente.
-   Los objetos que existen en la raíz del contexto de nomenclatura, como un dominio o una partición de aplicación, no se pueden restaurar.
-   Los objetos de esquema no se pueden restaurar. Los objetos de esquema no deben eliminarse nunca.
-   Es posible restaurar los contenedores eliminados, pero la restauración de los objetos eliminados que estaban en el contenedor antes de la eliminación es difícil porque la estructura de árbol del contenedor debe reconstruirse manualmente.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Permisos necesarios para restaurar un objeto eliminado

Cuando se elimina un objeto, se conserva el descriptor de seguridad del objeto. Aunque el propietario se puede identificar desde el descriptor de seguridad, por motivos de seguridad, solo los administradores de dominio pueden restaurar los objetos eliminados. Los administradores de dominio pueden conceder el permiso para restaurar los objetos de eliminación a otros usuarios y grupos; para ello, se concede al usuario o grupo el derecho de acceso de control "reanimación de marcadores de exclusión". El derecho de acceso de control "reanimar marcadores de exclusión" se concede en la raíz del contexto de nomenclatura. Solo los usuarios con permiso de acceso de lectura en un objeto y sus atributos pueden leer el objeto y los atributos accesibles una vez eliminado el objeto.

> [!Note]  
> Conceder a un usuario este permiso puede suponer un riesgo para la seguridad porque podría permitir al usuario restaurar un objeto de cuenta que tiene acceso a los recursos a los que el usuario no tendría acceso normalmente. Al restaurar una cuenta, el usuario adquiere esencialmente el control de esta cuenta, ya que el usuario debe establecer la contraseña inicial en la cuenta cuando se restaure la cuenta.

 

Para restaurar completamente un objeto eliminado, el usuario debe:

-   Tener o ser miembro de un grupo que tenga, el derecho de acceso de control "reanimación de marcadores de exclusión".

-   Tenga acceso de escritura para cada atributo obligatorio que requiere actualización.

-   Tener acceso de escritura al nombre distintivo relativo (RDN).

-   Tenga acceso de escritura a cada atributo opcional que deba actualizarse.

-   Tener derechos de creación secundarios en el contenedor de destino para la clase de objeto del objeto restaurado.

    > [!Note]  
    > El atributo **IsDeleted** no se comprueba durante la operación de restauración. Ni se comprobará el permiso Delete-Child en el contenedor "objetos eliminados".

     

## <a name="restoring-a-deleted-object"></a>Restaurar un objeto eliminado

Para restaurar un objeto eliminado, primero se debe encontrar el objeto en el contenedor de objetos eliminados. Para obtener más información sobre la recuperación de objetos eliminados, vea [recuperar objetos eliminados](retrieving-deleted-objects.md).

Cuando se encuentra el objeto, se deben completar las siguientes operaciones en una única operación LDAP. Esto requiere el uso de la [**función \_ \_ ext \_ s de LDAP Modify**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con el [**servidor LDAP para mostrar el control \_ \_ \_ \_ OID eliminado**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .

-   Quite el valor del atributo **IsDeleted** . El valor del atributo **IsDeleted** debe quitarse y no debe estar establecido en **false**.
-   Reemplace el nombre distintivo del objeto para que se mueva a un contenedor que no sea el contenedor de objetos eliminados. Puede ser cualquier contenedor que normalmente pueda contener el objeto. El nombre distintivo del contenedor anterior del objeto se puede encontrar en el atributo **lastKnownParent** del objeto eliminado. El atributo **lastKnownParent** solo se establece si el objeto se eliminó en un controlador de dominio de Windows Server 2003. Por lo tanto, es posible que el contenido del atributo **lastKnownParent** sea inexacto.
-   Restaure los atributos obligatorios para el objeto que se borró durante la eliminación.

> [!Note]  
> El atributo **objectCategory** también se puede establecer cuando se restaura el objeto, pero no es necesario. Si no se especifica ningún valor **objectCategory** , se utiliza el **objectCategory** predeterminado para el objeto **objectClass** .

 

Una vez restaurado el objeto, se puede obtener acceso a él como estaba antes de eliminarlo. En este momento, se deben restaurar todos los atributos opcionales que sean importantes. También se deben restaurar las referencias al objeto desde otros objetos del directorio.

Como medida de seguridad, los objetos de usuario se deshabilitan cuando se restauran. Los objetos de usuario deben estar habilitados después de restaurar los atributos opcionales para permitir el uso del objeto de usuario.

Para obtener más información y un ejemplo de código que muestra cómo restaurar un objeto eliminado, vea la siguiente función RestoreDeletedObject.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

En el ejemplo de código de C++ siguiente se muestra cómo restaurar un objeto eliminado.


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



 

 