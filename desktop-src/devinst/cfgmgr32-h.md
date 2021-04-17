---
title: 'Cfgmgr32.h '
description: Esta sección contiene temas de referencia para el encabezado Cfgmgr32. h.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ccc2baf458fea5e20842c9bfa60028c2cb8e23
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105665877"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

Esta sección contiene temas de referencia para el encabezado Cfgmgr32. h.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>La estructura de BUSNUMBER_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso del número de bus para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>La estructura BUSNUMBER_RANGE especifica una lista de requisitos de recursos que describe el uso del número de bus para una instancia de dispositivo. Para obtener más información acerca de las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>La estructura BUSNUMBER_RESOURCE especifica una lista de recursos o una lista de requisitos de recursos que describe el uso del número de bus para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>La función <strong>CM_Add_Empty_Log_Conf</strong> crea una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>vacía, para un tipo de configuración especificado y una instancia de dispositivo especificada, en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> .
</blockquote>
<br/> La función <strong>CM_Add_Empty_Log_Conf_Ex</strong> crea una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>vacía, para un tipo de configuración especificado y una instancia de dispositivo especificada, en el equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>La función <strong>CM_Add_ID</strong> anexa un identificador de <a href="/windows-hardware/drivers/install/device-ids">dispositivo</a> especificado (si aún no existe) a la lista de <a href="/windows-hardware/drivers/install/hardware-ids">identificadores de hardware</a> o a la lista de <a href="/windows-hardware/drivers/install/compatible-ids">identificadores compatibles</a> <a href="/windows-hardware/drivers/">de una instancia de dispositivo</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> .
</blockquote>
<br/> La función <strong>CM_Add_ID_Ex</strong> anexa un <a href="/windows-hardware/drivers/install/device-ids">identificador de dispositivo</a> (si aún no existe) a la lista de <a href="/windows-hardware/drivers/install/hardware-ids">identificadores de hardware</a> de una instancia de dispositivo o a una lista de <a href="/windows-hardware/drivers/install/compatible-ids">identificadores compatibles</a> , en el equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>La función <strong>CM_Add_Res_Des</strong> agrega un <a href="/windows-hardware/drivers/">descriptor de recursos</a> a una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> .
</blockquote>
<br/> La función <strong>CM_Add_Res_Des_Ex</strong> agrega un <a href="/windows-hardware/drivers/">descriptor de recursos</a> a una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>. La configuración lógica puede estar en el equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, se ha quitado la funcionalidad de acceso a equipos remotos. No se puede tener acceso a los equipos remotos cuando se ejecutan en estas versiones de Windows.
</blockquote>
<br/> La función <strong>CM_Connect_Machine</strong> crea una conexión a un equipo remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>La función <strong>CM_Delete_Class_Key</strong> quita la clase de <a href="/windows-hardware/drivers/">dispositivo</a> instalada especificada del sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>La función <strong>CM_Delete_Device_Interface_Key</strong> elimina la subclave del registro que usan las aplicaciones y los controladores para almacenar información específica de la interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La función <strong>CM_Delete_Device_Interface_Key_ExA</strong> elimina la subclave del registro que usan las aplicaciones y los controladores para almacenar información específica de la interfaz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La función <strong>CM_Delete_Device_Interface_Key_ExW</strong> elimina la subclave del registro que usan las aplicaciones y los controladores para almacenar información específica de la interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>La función <strong>CM_Delete_DevNode_Key</strong> elimina las claves del registro disponibles para el usuario que están asociadas a un dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>La función <strong>CM_Disable_DevNode</strong> deshabilita un dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, se ha quitado la funcionalidad de acceso a equipos remotos. No se puede tener acceso a los equipos remotos cuando se ejecutan en estas versiones de Windows.
</blockquote>
<br/> La función <strong>CM_Disconnect_Machine</strong> quita una conexión a un equipo remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>La función <strong>CM_Enable_DevNode</strong> habilita un dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>La función <strong>CM_Enumerate_Classes</strong> , cuando se llama repetidamente, enumera las <a href="/windows-hardware/drivers/">clases de dispositivo</a> instaladas del equipo local proporcionando el GUID de cada clase.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> .
</blockquote>
<br/> La función <strong>CM_Enumerate_Classes_Ex</strong> , cuando se llama repetidamente, enumera <a href="/windows-hardware/drivers/">las clases de dispositivo</a>instaladas de un equipo local o remoto, proporcionando el GUID de cada clase.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>La función <strong>CM_Enumerate_Enumerators</strong> enumera los enumeradores de dispositivos del equipo local proporcionando el nombre de cada enumerador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> .
</blockquote>
<br/> La función <strong>CM_Enumerate_Enumerators_Ex</strong> enumera los enumeradores de dispositivos de un equipo local o remoto, proporcionando el nombre de cada enumerador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>La función <strong>CM_Free_Log_Conf</strong> quita una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> y todos los <a href="/windows-hardware/drivers/">descriptores de recursos</a> asociados del equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> .
</blockquote>
<br/> La función <strong>CM_Free_Log_Conf_Ex</strong> quita una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> y todos los <a href="/windows-hardware/drivers/">descriptores de recursos</a> asociados de un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>La función <strong>CM_Free_Log_Conf_Handle</strong> invalida un identificador de configuración lógico y libera su asignación de memoria asociada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>La función <strong>CM_Free_Res_Des</strong> quita un <a href="/windows-hardware/drivers/">descriptor de recursos</a> de una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> .
</blockquote>
<br/> La función <strong>CM_Free_Res_Des_Ex</strong> quita un <a href="/windows-hardware/drivers/">descriptor de recursos</a> de una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>La función <strong>CM_Free_Res_Des_Handle</strong> invalida un identificador de descripción de recursos y libera la asignación de memoria asociada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>La función <strong>CM_Free_Resource_Conflict_Handle</strong> invalida un identificador de una lista de conflictos de recursos y libera la asignación de memoria asociada del identificador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>La función <strong>CM_Get_Child</strong> se usa para recuperar un identificador de instancia de dispositivo en el primer nodo secundario de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de la máquina local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Child_Ex</strong> se usa para recuperar un identificador de instancia de dispositivo en el primer nodo secundario de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de un equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>La función <strong>CM_Get_Class_Property</strong> recupera una propiedad de dispositivo que se establece para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo</a> o de instalación de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivos</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Class_Property_ExW</strong> recupera una propiedad de dispositivo que se establece para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo</a> o de instalación de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivos</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>La función <strong>CM_Get_Class_Property_Keys</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo</a> o de instalación de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivos</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Class_Property_Keys_Ex</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo</a> o de instalación de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivos</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>La función <strong>CM_Get_Class_Registry_Property</strong> recupera una <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">propiedad de clase de instalación de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>La función <strong>CM_Get_Depth</strong> se usa para obtener la profundidad de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el árbol de <a href="/windows-hardware/drivers/kernel/device-tree">dispositivos</a>de la máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Depth_Ex</strong> se usa para obtener la profundidad de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) dentro del <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_ID</strong> recupera el <a href="/windows-hardware/drivers/install/device-instance-ids">identificador de instancia de dispositivo</a> para una <a href="/windows-hardware/drivers/">instancia de dispositivo</a> especificada en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Device_ID_Ex</strong> recupera el <a href="/windows-hardware/drivers/install/device-instance-ids">identificador de instancia de dispositivo</a> para una <a href="/windows-hardware/drivers/">instancia de dispositivo</a> especificada en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_ID_List</strong> recupera una lista de <a href="/windows-hardware/drivers/install/device-instance-ids">identificadores de instancia de dispositivo</a> para las instancias de <a href="/windows-hardware/drivers/">dispositivo</a>del equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Device_ID_List_Ex</strong> recupera una lista de <a href="/windows-hardware/drivers/install/device-instance-ids">identificadores de instancia de dispositivo</a> para las instancias de <a href="/windows-hardware/drivers/">dispositivo</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_ID_List_Size</strong> recupera el tamaño de búfer necesario para contener una lista de <a href="/windows-hardware/drivers/install/device-instance-ids">identificadores de instancia de dispositivo</a> para las <a href="/windows-hardware/drivers/">instancias de dispositivo</a>del equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Device_ID_List_Size_Ex</strong> recupera el tamaño del búfer necesario para contener una lista de <a href="/windows-hardware/drivers/install/device-instance-ids">identificadores de instancia de dispositivo</a> para <a href="/windows-hardware/drivers/">las instancias de dispositivo</a>de un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_ID_Size</strong> recupera el tamaño de búfer necesario para contener un <a href="/windows-hardware/drivers/install/device-instance-ids">identificador de instancia de dispositivo</a> para una <a href="/windows-hardware/drivers/">instancia de dispositivo</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Device_ID_Size_Ex</strong> recupera el tamaño de búfer necesario para contener un <a href="/windows-hardware/drivers/install/device-instance-ids">identificador de instancia de dispositivo</a> para una <a href="/windows-hardware/drivers/">instancia de dispositivo</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_Interface_Alias</strong> devuelve el alias de la instancia de interfaz de dispositivo especificada, si el alias existe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_Interface_List</strong> recupera una lista de instancias de la interfaz de dispositivo que pertenecen a una <a href="/windows-hardware/drivers/install/device-interface-classes">clase de interfaz de dispositivo</a>especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_Interface_List_Size</strong> recupera el tamaño del búfer que se debe pasar a la función <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_Interface_Property</strong> recupera una propiedad de dispositivo que se establece para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Device_Interface_Property_ExW</strong> recupera una propiedad de dispositivo que se establece para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>La función <strong>CM_Get_Device_Interface_Property_Keys</strong> recupera una matriz de claves de propiedad de dispositivo que representan las propiedades del dispositivo que se establecen para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> recupera una matriz de claves de propiedad de dispositivo que representan las propiedades del dispositivo que se establecen para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>La función <strong>CM_Get_DevNode_Property</strong> recupera una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_DevNode_Property_ExW</strong> recupera una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>La función <strong>CM_Get_DevNode_Property_Keys</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una instancia del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_DevNode_Property_Keys_Ex</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una instancia del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>La función <strong>CM_Get_DevNode_Registry_Property</strong> recupera una propiedad de dispositivo especificada del registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>La función <strong>CM_Get_DevNode_Status</strong> obtiene el estado de una instancia de dispositivo desde su nodo de dispositivo (<a href="/windows-hardware/drivers/">DevNode</a>) en el árbol de <a href="/windows-hardware/drivers/kernel/device-tree">dispositivos</a>de la máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_DevNode_Status_Ex</strong> obtiene el estado de una instancia de dispositivo desde su nodo de dispositivo (<a href="/windows-hardware/drivers/">DevNode</a>) en el <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>La función <strong>CM_Get_First_Log_Conf</strong> obtiene la primera <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>, de un tipo de configuración especificado, asociada a una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> especificada en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_First_Log_Conf_Ex</strong> obtiene la primera <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> asociada a una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> especificada en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso y no debe usarse.
</blockquote>
<br/> La función <strong>CM_Get_HW_Prof_Flags</strong> recupera las marcas de configuración específicas del <a href="/windows-hardware/drivers/">Perfil de hardware</a>para una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> en un equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función está en desuso y no debe usarse.
</blockquote>
<br/> La función <strong>CM_Get_HW_Prof_Flags_Ex</strong> recupera las marcas de configuración específicas del <a href="/windows-hardware/drivers/">Perfil de hardware</a>para una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> en un equipo remoto o en un equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>La función <strong>CM_Get_Log_Conf_Priority</strong> obtiene la prioridad de configuración de una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> especificada en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Log_Conf_Priority_Ex</strong> obtiene la prioridad de configuración de una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> especificada en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>La función <strong>CM_Get_Next_Log_Conf</strong> obtiene la siguiente <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> asociada a una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> específica en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Next_Log_Conf_Ex</strong> obtiene la siguiente <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> asociada a una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> específica en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>La función <strong>CM_Get_Next_Res_Des</strong> obtiene un identificador para el siguiente <a href="/windows-hardware/drivers/">descriptor de recursos</a>, de un tipo de recurso especificado, para una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Next_Res_Des_Ex</strong> obtiene un identificador para el siguiente <a href="/windows-hardware/drivers/">descriptor de recursos</a>, de un tipo de recurso especificado, para una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>La función <strong>CM_Get_Parent</strong> obtiene un identificador de instancia de dispositivo para el nodo primario de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el árbol de dispositivos de la máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Parent_Ex</strong> obtiene un identificador de instancia de dispositivo para el nodo primario de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>La función <strong>CM_Get_Res_Des_Data</strong> recupera la información almacenada en un <a href="/windows-hardware/drivers/">descriptor de recursos</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Res_Des_Data_Ex</strong> recupera la información almacenada en un <a href="/windows-hardware/drivers/">descriptor de recursos</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>La función <strong>CM_Get_Res_Des_Data_Size</strong> obtiene el tamaño del búfer necesario para contener la información contenida en un <a href="/windows-hardware/drivers/">descriptor de recursos</a> especificado en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Res_Des_Data_Size_Ex</strong> obtiene el tamaño del búfer necesario para contener la información contenida en un <a href="/windows-hardware/drivers/">descriptor de recursos</a> especificado en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>La función <strong>CM_Get_Resource_Conflict_Count</strong> obtiene el número de conflictos contenidos en una lista de conflictos de recursos especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>La función <strong>CM_Get_Resource_Conflict_Details</strong> obtiene los detalles sobre uno de los conflictos de recursos en una lista de conflictos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>La función <strong>CM_Get_Sibling</strong> obtiene un identificador de instancia de dispositivo para el siguiente nodo relacionado de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de la máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> .
</blockquote>
<br/> La función <strong>CM_Get_Sibling_Ex</strong> obtiene un identificador de instancia de dispositivo para el siguiente nodo relacionado de un nodo de dispositivo especificado, en el <a href="/windows-hardware/drivers/kernel/device-tree">árbol de dispositivos</a>de un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso y no debe usarse.
</blockquote>
<br/> La función <strong>CM_Get_Version</strong> devuelve la versión 4,0 del plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) de un equipo local. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso y no debe usarse.
</blockquote>
<br/> La función <strong>CM_Get_Version_Ex</strong> devuelve la versión 4,0 del plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) para un equipo local o remoto. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>La función <strong>CM_Is_Dock_Station_Present</strong> identifica si una <a href="/windows-hardware/drivers/">estación de acoplamiento</a> está presente en un equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> .
</blockquote>
<br/> La función <strong>CM_Is_Dock_Station_Present_Ex</strong> identifica si una <a href="/windows-hardware/drivers/">estación de acoplamiento</a> está presente en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso y no debe usarse.
</blockquote>
<br/> La función <strong>CM_Is_Version_Available</strong> indica si un equipo local admite una versión especificada de plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso y no debe usarse.
</blockquote>
<br/> La función <strong>CM_Is_Version_Available_Ex</strong> indica si una versión especificada de plug and Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">dll</a> (<em>Cfgmgr32.dll</em>) es compatible con una máquina local o remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>La función <strong>CM_Locate_DevNode</strong> obtiene un identificador de instancia de dispositivo para el nodo de dispositivo que está asociado a un <a href="/windows-hardware/drivers/install/device-instance-ids">identificador de instancia de dispositivo</a> especificado en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> .
</blockquote>
<br/> La función <strong>CM_Locate_DevNode_Ex</strong> obtiene un identificador de instancia de dispositivo para el nodo de dispositivo que está asociado a un <a href="/windows-hardware/drivers/install/device-instance-ids">identificador de instancia de dispositivo</a>especificado, en un equipo local o en un equipo remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Convierte un código <strong>CONFIGRET</strong> especificado en su código de error del sistema equivalente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>La función <strong>CM_Modify_Res_Des</strong> modifica un descriptor de recursos especificado en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> .
</blockquote>
<br/> La función <strong>CM_Modify_Res_Des_Ex</strong> modifica un descriptor de recursos especificado en un equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Esta enumeración identifica Plug and Play tipos de evento de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Esta es una estructura de datos de eventos de notificación de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Estructura de filtro de notificación de dispositivo<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>La función <strong>CM_Open_Class_Key</strong> abre la clave del registro de la clase de instalación de dispositivos, la clave del registro de la clase de interfaz de dispositivo o una subclave específica de una clase.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>La función <strong>CM_Open_Device_Interface_Key</strong> abre la subclave del registro que usan las aplicaciones y los controladores para almacenar información específica de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La función <strong>CM_Open_Device_Interface_Key_ExA</strong> abre la subclave del registro que usan las aplicaciones y los controladores para almacenar información específica de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> .
</blockquote>
<br/> La función <strong>CM_Open_Device_Interface_Key_ExW</strong> abre la subclave del registro que usan las aplicaciones y los controladores para almacenar información específica de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>La función <strong>CM_Open_DevNode_Key</strong> abre una clave del registro para la información de configuración específica del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>La función <strong>CM_Query_And_Remove_SubTree</strong> comprueba si una instancia de dispositivo y sus elementos secundarios se pueden quitar y, en ese caso, los quita.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> .
</blockquote>
<br/> La función <strong>CM_Query_And_Remove_SubTree_Ex</strong> comprueba si una instancia de dispositivo y sus elementos secundarios se pueden quitar y, en ese caso, los quita.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>La función <strong>CM_Query_Resource_Conflict_List</strong> identifica las instancias de dispositivo que tienen requisitos de recursos que entran en conflicto con la descripción de recursos de una instancia de dispositivo especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>La función <strong>CM_Reenumerate_DevNode</strong> enumera los dispositivos identificados por un nodo de dispositivo especificado y todos sus elementos secundarios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> .
</blockquote>
<br/> La función <strong>CM_Reenumerate_DevNode_Ex</strong> enumera los dispositivos identificados por un nodo de dispositivo especificado y todos sus elementos secundarios.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Use <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a> en lugar de <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> si el código tiene como destino Windows 7 o versiones anteriores de Windows. Los autores de llamadas de modo kernel deben usar <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> en su lugar.<br/> La función <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> registra una rutina de devolución de llamada de aplicación a la que se llamará cuando se produzca un evento PNP con el tipo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>La función <strong>CM_Request_Device_Eject</strong> prepara una instancia de dispositivo local para su eliminación segura, si el dispositivo es extraíble. Si el dispositivo se puede expulsar físicamente, será.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> .
</blockquote>
<br/> La función <strong>CM_Request_Device_Eject_Ex</strong> prepara una instancia de dispositivo local o remota para su eliminación segura, si el dispositivo es extraíble. Si el dispositivo se puede expulsar físicamente, será.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>La función <strong>CM_Request_Eject_PC</strong> solicita que se expulse un PC portátil, que se inserta en una <a href="/windows-hardware/drivers/">estación de acoplamiento</a>local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> .
</blockquote>
<br/> La función <strong>CM_Request_Eject_PC_Ex</strong> solicita que se expulse un PC portátil, que se inserta en una <a href="/windows-hardware/drivers/">estación de acoplamiento</a>local o remota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>La función <strong>CM_Set_Class_Property</strong> establece una propiedad de clase para una clase de instalación de dispositivo o una clase de interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> .
</blockquote>
<br/> La función <strong>CM_Set_Class_Property_ExW</strong> establece una propiedad de clase para una clase de instalación de dispositivo o una clase de interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>La función <strong>CM_Set_Class_Registry_Property</strong> establece o elimina una propiedad de una <a href="/windows-hardware/drivers/install/device-setup-classes">clase de instalación de dispositivos</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>La función <strong>CM_Set_Device_Interface_Property</strong> establece una propiedad de dispositivo de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> .
</blockquote>
<br/> La función <strong>CM_Set_Device_Interface_Property_ExW</strong> establece una propiedad de dispositivo de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>La función <strong>CM_Set_DevNode_Problem</strong> establece un código de problema para un dispositivo que está instalado en un equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> .
</blockquote>
<br/> La función <strong>CM_Set_DevNode_Problem_Ex</strong> establece un código de problema para un dispositivo que se instala en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>La función <strong>CM_Set_DevNode_Property</strong> establece una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012, esta función está en desuso. En su lugar, use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> .
</blockquote>
<br/> La función <strong>CM_Set_DevNode_Property_ExW</strong> establece una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>La función <strong>CM_Set_DevNode_Registry_Property</strong> establece una propiedad de dispositivo especificada en el registro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>La función <strong>CM_Setup_DevNode</strong> reinicia una instancia de dispositivo que no se está ejecutando porque hay un problema con la configuración del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>La función <strong>CM_Uninstall_DevNode</strong> quita todo el estado persistente asociado a una instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Use <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a> en lugar de <strong>CM_Unregister_Notification</strong> si el código tiene como destino Windows 7 o versiones anteriores de Windows.<br/> La función <strong>CM_Unregister_Notification</strong> cierra el identificador HCMNOTIFICATION especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>La función <strong>CMP_WaitNoPendingInstallEvents</strong> espera hasta que no haya actividades de instalación de dispositivos pendientes para que el administrador de PNP realice la acción.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>La estructura CONFLICT_DETAILS se utiliza como parámetro para la función <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>La estructura de CS_DES se usa para especificar una lista de recursos que describe el uso de recursos específicos de la clase de dispositivo para una instancia de dispositivo. Para obtener más información acerca de las listas de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>La estructura de CS_RESOURCE se usa para especificar una lista de recursos que describe el uso de recursos específicos de la clase de dispositivo para una instancia de dispositivo. Para obtener más información acerca de las listas de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>La estructura de DMA_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de canales de acceso directo a memoria (DMA) para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>La estructura DMA_RANGE especifica una lista de requisitos de recursos que describe el uso del canal DMA para una instancia de dispositivo. Para obtener más información acerca de las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>La estructura de DMA_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso del canal DMA para una instancia de dispositivo. Para obtener más información acerca de las listas de requisitos de recursos y listas de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>La estructura de IO_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de puertos de e/s para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>La estructura IO_RANGE especifica una lista de requisitos de recursos que describe el uso del puerto de e/s para una instancia de dispositivo. Para obtener más información acerca de las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>La estructura de IO_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de puertos de e/s para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>La estructura de IRQ_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de la línea de IRQ para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>La estructura IRQ_RANGE especifica una lista de requisitos de recursos que describe el uso de la línea de IRQ para una instancia de dispositivo. Para obtener más información acerca de las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>La estructura de IRQ_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de la línea de IRQ para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>La estructura de MEM_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de memoria para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>La estructura MEM_RANGE especifica una lista de requisitos de recursos que describe el uso de memoria para una instancia de dispositivo. Para obtener más información acerca de las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>La estructura de MEM_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de memoria para una instancia de dispositivo. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>La estructura de MFCARD_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de recursos por parte de <em>una</em> de las funciones de hardware proporcionadas por una instancia de un dispositivo multifunción. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>La estructura de MFCARD_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de recursos por parte de <em>una</em> de las funciones de hardware proporcionadas por una instancia de un dispositivo multifunción. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>La estructura de PCCARD_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de recursos por parte de una instancia de tarjeta PC. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>La estructura de PCCARD_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de recursos por parte de una instancia de tarjeta PC. Para obtener más información sobre listas de recursos y listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">recursos de hardware</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 

[Enviar comentarios acerca de este tema a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Enviar comentarios acerca de este tema a Microsoft")