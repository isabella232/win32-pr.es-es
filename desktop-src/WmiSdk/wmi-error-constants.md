---
description: Si se produce un error, WMI devuelve un código de error como un valor HRESULT. Estos códigos pueden devolverse mediante scripts, aplicaciones de C++ o Wmic.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Constantes de error wmi (WbemCli.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569693"
---
# <a name="wmi-error-constants"></a>Constantes de error wmi

Si se produce un error, WMI devuelve un código de error como **un valor HRESULT.** Estos códigos pueden devolverse mediante scripts, aplicaciones de C++ o [**Wmic**](wmic.md).

> [!Note]
>
> La siguiente documentación está dirigida a desarrolladores y administradores de TI. Si es un usuario final que ha experimentado un mensaje de error sobre WMI, debe ir a [Soporte técnico de Microsoft](https://support.microsoft.com/) y buscar el código de error que ve en el mensaje de error. Para obtener más información sobre cómo solucionar problemas con scripts WMI y el servicio WMI, vea [WMI isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI. Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI. En cualquier caso, no elimine el repositorio WMI como primera acción porque la eliminación del repositorio puede causar daños en el sistema o en las aplicaciones instaladas.
>
> Para obtener más información sobre el origen del problema, puede descargar y ejecutar la Utilidad de diagnóstico de WMI [línea](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de comandos de diagnóstico. Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo. El informe también ayuda a los servicios de soporte técnico de Microsoft a ayudarle. Puede descargar la Utilidad de diagnóstico de WMI [aquí.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

 

Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de red (por ejemplo, 64). Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema. Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: El nombre de red especificado ya no está disponible.

En la lista siguiente se enumeran algunos intervalos comunes de errores.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068: 0x80041099
</dt> <dd>

Errores que se originan en el propio WMI.

Error en una operación WMI específica debido a

-   Se produce un error en la solicitud, por ejemplo, se produce un error en una consulta WQL o la cuenta no tiene los permisos correctos.
-   Un problema de infraestructura WMI, como un registro CIM o DCOM incorrecto.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Errores que se origina en el sistema operativo principal. WMI puede devolver este tipo de error debido a un error externo, por ejemplo, error de seguridad de DCOM.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Errores que se origina en DCOM. Por ejemplo, la configuración de DCOM para las operaciones en un equipo remoto puede ser incorrecta.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Error que se origina en ADSI (interfaces de servicio Active Directory) o LDAP (protocolo ligero de acceso a directorios), por ejemplo, un error de acceso Active Directory al usar los proveedores de Active Directory WMI.

</dd> </dl>

Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de red (por ejemplo, 64). Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema. Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: El nombre de red especificado ya no está disponible. En C++, puede llamar a [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) y especificar **C: \\ Windows \\ System32 \\ wbem \\wmiutils.dll** como módulo de mensaje.

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ FAILED**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Error de llamada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



No se encuentra el objeto .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



El usuario actual no tiene permiso para realizar la acción.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**ERROR DEL PROVEEDOR WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



El proveedor ha dado error en algún momento distinto de durante la inicialización.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Error de coincidencia de tipos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ OUT \_ OF \_ MEMORY**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



No hay suficiente memoria para la operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM \_ E CONTEXTO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



El [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) no es válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM \_ E \_ INVALID \_ PARAMETER**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Uno de los parámetros de la llamada no es correcto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ NO \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



El recurso, normalmente un servidor remoto, no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM \_ E \_ CRITICAL \_ ERROR**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A)
</dt> <dt>



Error interno, crítico e inesperado. Informe del error al soporte técnico de Microsoft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM \_ E \_ INVALID \_ STREAM**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B)
</dt> <dt>



Se dañó uno o más paquetes de red durante una sesión remota.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E NO SE \_ \_ ADMITE**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



No se admite la característica u operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM \_ E \_ SUPERCLASS NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D)
</dt> <dt>



La clase primaria especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E ESPACIO DE NOMBRES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



No se encuentra el espacio de nombres especificado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ INVALID \_ OBJECT**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



La instancia especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM \_ E \_ INVALID \_ CLASS**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



La clase especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**NO SE ENCONTRÓ EL PROVEEDOR WBEM \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



El proveedor al que se hace referencia en el esquema no tiene un registro correspondiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM \_ E REGISTRO DE PROVEEDOR NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



El proveedor al que se hace referencia en el esquema tiene un registro incorrecto o incompleto.

Este error puede deberse a muchas condiciones, incluidas las siguientes:

-   Falta un [ \# comando de espacio de nombres pragma](pragma-namespace.md) en Managed Object Format archivo (MOF) usado para registrar el proveedor. El proveedor puede estar registrado en el espacio de nombres WMI incorrecto.
-   Error al recuperar el registro COM.
-   El modelo de hospedaje no es válido. Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).
-   Una clase especificada en el registro no es válida.
-   Error al crear una instancia de o heredar de la [**\_ \_ clase Win32Provider**](--win32provider.md) para crear el registro del proveedor en el archivo MOF.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM \_ E \_ PROVIDER \_ LOAD \_ FAILURE**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM no encuentra un proveedor al que se hace referencia en el esquema.

Este error puede deberse a muchas condiciones, incluidas las siguientes:

-   El proveedor usa un archivo DLL de WMI que no coincide con el archivo .lib usado cuando se creó el proveedor.
-   El archivo DLL del proveedor, o cualquiera de los archivos DLL de los que depende, está dañado.
-   El proveedor no pudo exportar [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).
-   El proveedor en proceso no se registró mediante **el comando regsvr32.**
-   El proveedor fuera de proceso no se registró mediante el **modificador /regserver.** Por ejemplo, **myprog.exe /regserver**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**ERROR DE INICIALIZACIÓN DE WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



El componente, como un proveedor, no se pudo inicializar por motivos internos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM \_ E \_ TRANSPORT \_ FAILURE**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Error de red que impide el funcionamiento normal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM \_ E \_ INVALID \_ OPERATION**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



La operación solicitada no es válida. Normalmente, este error está relacionado con intentos no válidos de eliminar clases o propiedades.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ INVALID \_ QUERY**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La consulta no era válida sintácticamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM \_ E TIPO DE CONSULTA NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



No se admite el lenguaje de consulta solicitado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



En una operación put, se especificó la marca **wbemChangeFlagCreateOnly,** pero la instancia ya existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM \_ E \_ OVERRIDE \_ NOT \_ ALLOWED**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A)
</dt> <dt>



No es posible realizar la operación de adición en este calificador porque el objeto propietario no permite invalidaciones.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**CALIFICADOR \_ \_ PROPAGADO WBEM E \_**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B)
</dt> <dt>



El usuario intentó eliminar un calificador que no era propiedad de . Se trataba de un calificador heredado de una clase principal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM \_ E \_ PROPAGATED \_ PROPERTY**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C)
</dt> <dt>



El usuario intentó eliminar una propiedad que no era de su propiedad. Se trataba de una propiedad heredada de una clase principal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ UNEXPECTED**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D)
</dt> <dt>



El cliente realizó una secuencia inesperada e no conforme de llamadas, como llamar a [**EndEnumeration antes**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) de llamar [**a BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**OPERACIÓN NO ILEGAL DE WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E)
</dt> <dt>



El usuario solicitó una operación no ilegal, como generar una clase a partir de una instancia de .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E NO PUEDE SER \_ \_ \_ CLAVE**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F)
</dt> <dt>



Intento no válido de especificar un calificador de clave en una propiedad que no puede ser una clave. Las claves se especifican en la definición de la clase de un objeto, y no se pueden modificar instancia por instancia.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM \_ E \_ INCOMPLETE \_ (CLASE)**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



El objeto actual no es una definición de clase válida. Está incompleto o no se ha registrado con WMI mediante [**SWbemObject.Put \_**](swbemobject-put-.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM \_ E \_ SINTAXIS NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La consulta no es válida sintácticamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM \_ E \_ \_ NONDECORATED (OBJETO)**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Se intentó modificar una propiedad de solo lectura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ PROVIDER \_ NOT \_ CAPABLE**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



El proveedor no puede realizar la operación solicitada. Esto puede incluir una consulta demasiado compleja, recuperar una instancia, crear o actualizar una clase, eliminar una clase o enumerar una clase.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E CLASS TIENE ELEMENTOS \_ \_ \_ SECUNDARIOS**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



Se intentó realizar un cambio que invalida una subclase.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM \_ E CLASS TIENE \_ \_ \_ INSTANCIAS**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



Se intentó eliminar o modificar una clase que tiene instancias de .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM \_ E \_ QUERY \_ NOT \_ IMPLEMENTED**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ ILLEGAL \_ NULL**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Se especificó el valor **nothing/NULL** para una propiedad que debe tener un valor, como uno marcado por un calificador [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md)o **Not \_ Null.**


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM \_ E \_ INVALID \_ QUALIFIER \_ TYPE**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



Se proporcionó un valor variant para un calificador que no es un tipo de calificador legal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM \_ E \_ INVALID \_ PROPERTY \_ TYPE**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A)
</dt> <dt>



El tipo CIM especificado para una propiedad no es válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ VALUE \_ OUT \_ OF \_ RANGE**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La solicitud se realizó con un valor fuera del intervalo o no es compatible con el tipo .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E NO PUEDE SER \_ \_ \_ SINGLETON**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C)
</dt> <dt>



Se intentó no hacer una clase singleton, como cuando la clase se deriva de una clase que no es singleton.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ INVALID \_ CIM \_ TYPE**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D)
</dt> <dt>



El tipo CIM especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ INVALID \_ METHOD**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



El método solicitado no está disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E PARÁMETROS DE MÉTODO NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Los parámetros proporcionados para el método no son válidos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM \_ E \_ SYSTEM \_ PROPERTY**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Se intentó obtener calificadores en una propiedad del sistema.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM \_ E \_ INVALID \_ PROPERTY**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



No se reconoce el tipo de propiedad.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM \_ E \_ CALL \_ CANCELLED**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



El proceso asincrónico se ha cancelado internamente o por el usuario. Tenga en cuenta que debido al tiempo y la naturaleza de la operación asincrónica, es posible que la operación no se haya cancelado realmente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ SHUTTING \_ DOWN**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



El usuario ha solicitado una operación mientras WMI está en proceso de apagado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**MÉTODO \_ PROPAGADO WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



Se intentó reutilizar un nombre de método existente de una clase primaria y las firmas no coinciden.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM \_ E PARÁMETRO NO \_ \_ ADMITIDO**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Uno o más valores de parámetro, como un texto de consulta, es demasiado complejo o no se admite. Por lo tanto, se solicita a WMI que vuelva a intentar la operación con parámetros más sencillos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ E \_ MISSING \_ PARAMETER \_ ID**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



Faltaba el parámetro en la llamada al método.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM \_ E \_ INVALID \_ PARAMETER \_ ID**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



El parámetro de método tiene [**un calificador de**](standard-wmi-qualifiers.md) identificador que no es válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM \_ E \_ NONCONSECUTIVE \_ PARAMETER \_ IDS**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Uno o varios de los parámetros de método tienen [**calificadores de**](standard-wmi-qualifiers.md) identificador que están fuera de la secuencia.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM \_ E \_ PARAMETER \_ ID \_ ON \_ RETVAL**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



El valor devuelto para un método tiene un [**calificador de**](standard-wmi-qualifiers.md) identificador.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E RUTA DE ACCESO DE OBJETO NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



La ruta de acceso de objeto especificada no era válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E FUERA DEL ESPACIO EN \_ \_ \_ \_ DISCO**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B)
</dt> <dt>



El disco no tiene espacio o se alcanza el límite de 4 GB en el tamaño del repositorio WMI (repositorio CIM).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**BÚFER WBEM \_ E \_ DEMASIADO \_ \_ PEQUEÑO**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C)
</dt> <dt>



El búfer proporcionado era demasiado pequeño para contener todos los objetos del enumerador o para leer una propiedad de cadena.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM \_ E EXTENSIÓN PUT NO \_ \_ \_ ADMITIDA**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D)
</dt> <dt>



El proveedor no admite la operación put solicitada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM \_ E \_ UNKNOWN \_ OBJECT \_ TYPE**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E)
</dt> <dt>



Se encontró un objeto con un tipo o versión incorrectos durante la serialización.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM \_ E \_ UNKNOWN \_ PACKET \_ TYPE**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F)
</dt> <dt>



Se encontró un paquete con un tipo o versión incorrectos durante la serialización.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM \_ E \_ MARSHAL \_ VERSION \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



El paquete tiene una versión no admitida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM \_ E \_ MARSHAL \_ INVALID \_ SIGNATURE**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



Parece que el paquete está dañado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM \_ E \_ CALIFICADOR NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



Se intentó no coincide con los calificadores, como colocar \[ la clave en un objeto en lugar de en una \] propiedad.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM \_ E PARÁMETRO DUPLICADO NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



El parámetro duplicado se declaró en un método CIM.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ TOO \_ MUCH \_ DATA**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ SERVER \_ TOO \_ BUSY**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



Se ha dado un error en la llamada a [**IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) El proveedor puede volver a establecer el evento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM \_ E \_ INVALID \_ FLAVOR**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



El tipo de calificador especificado no era válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**REFERENCIA CIRCULAR DE WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



Se intentó crear una referencia que sea circular (por ejemplo, derivar una clase de sí misma).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ UNSUPPORTED \_ CLASS \_ UPDATE**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



No se admite la clase especificada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E NO PUEDE CAMBIAR LA HERENCIA DE \_ \_ \_ \_ CLAVES**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



Se intentó cambiar una clave cuando las instancias o subclases ya usan la clave.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E NO PUEDE CAMBIAR LA HERENCIA DE \_ \_ \_ \_ ÍNDICES**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



Se intentó cambiar un índice cuando las instancias o subclases ya usan el índice.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ \_ DEMASIADAS \_ PROPIEDADES**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



Se intentó crear más propiedades de las que admite la versión actual de la clase .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM \_ E \_ UPDATE \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



La propiedad se ha redefinido con un tipo en conflicto en una clase derivada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM \_ E \_ UPDATE \_ OVERRIDE \_ NOT \_ ALLOWED**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



Se intentó en una clase derivada invalidar un calificador que no se puede invalidar.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM \_ E \_ UPDATE \_ PROPAGATED \_ (MÉTODO PROPAGADO)**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



El método se declaró de nuevo con una firma en conflicto en una clase derivada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**MÉTODO WBEM \_ E \_ NO \_ \_ IMPLEMENTADO**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



Se intentó ejecutar un método no marcado con \[ implementado en ninguna clase \] pertinente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**MÉTODO WBEM \_ E \_ \_ DESHABILITADO**
</dt> <dd> <dl> <dt>


</dt> <dt>



Se intentó ejecutar un método marcado con \[ \] deshabilitado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM \_ E \_ REFRESHER \_ BUSY**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



El actualizador está ocupado con otra operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM \_ E \_ UNPARSABLE \_ QUERY**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



La consulta de filtrado no es válida sintácticamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ NOT \_ (CLASE DE \_ EVENTOS)**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



La cláusula FROM de una consulta de filtrado hace referencia a una clase que no es una clase de evento (no derivada de [**\_ \_ Event**](--event.md)).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ MISSING \_ GROUP \_ WITHIN**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A)
</dt> <dt>



Se utilizó una cláusula GROUP BY sin la cláusula GROUP WITHIN correspondiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ MISSING \_ AGGREGATION \_ LIST**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B)
</dt> <dt>



Se utilizó una cláusula GROUP BY. No se admite la agregación en todas las propiedades.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM \_ E \_ PROPERTY \_ NOT \_ AN \_ OBJECT**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C)
</dt> <dt>



Se utilizó la notación de punto en una propiedad que no es un objeto incrustado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ AGGREGATING \_ BY \_ OBJECT**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D)
</dt> <dt>



Una cláusula GROUP BY hace referencia a una propiedad que es un objeto incrustado sin utilizar la notación de punto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM \_ E \_ UNINTERPRETABLE \_ PROVIDER \_ QUERY**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F)
</dt> <dt>



La consulta de registro del proveedor de eventos ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) no especificó las clases para las que se proporcionaron los eventos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ BACKUP \_ RESTORE \_ WINMGMT \_ RUNNING**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



Se realizó una solicitud para realizar una copia de seguridad o restaurar el repositorio mientras estaba en uso por WinMgmt.exe o por el proceso SVCHOST que contiene el servicio WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM \_ E \_ QUEUE \_ OVERFLOW**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



Cola de entrega asincrónica desbordada por el consumidor de eventos que es demasiado lenta.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM \_ E \_ PRIVILEGE \_ NOT \_ HELD**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



Error en la operación porque el cliente no tenía el privilegio de seguridad necesario.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM \_ E \_ INVALID \_ OPERATOR**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



El operador no es válido para este tipo de propiedad.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM E LOCAL CREDENTIALS (CREDENCIALES LOCALES DE WBEM \_ \_ \_ E)**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



El usuario especificó un nombre de usuario, contraseña o autoridad en una conexión local. El usuario debe usar un nombre de usuario o contraseña en blanco y confiar en la seguridad predeterminada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E NO PUEDE SER \_ \_ \_ ABSTRACT**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



La clase se ha hecho abstracta cuando su clase primaria no es abstracta.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E \_ AMENDED \_ (OBJETO)**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



El objeto modificado se escribió sin especificar la marca **WBEM \_ FLAG USE \_ \_ AMENDED \_ QUALIFIERS.**


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM \_ E \_ CLIENT \_ TOO \_ SLOW**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



El cliente no recuperó objetos lo suficientemente rápido de una enumeración. Esta constante se devuelve cuando un cliente crea un objeto de enumeración, pero no recupera objetos del enumerador de forma oportuna, lo que hace que se haga una copia de seguridad de las memorias caché de objetos del enumerador.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM \_ E \_ NULL \_ SECURITY \_ DESCRIPTOR**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



Se usó el descriptor de seguridad NULL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM \_ E \_ TIMED \_ OUT**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



Se ha pasado el tiempo de espera de la operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM \_ E \_ INVALID \_ ASSOCIATION**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



La asociación no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM \_ E \_ AMBIGUOUS \_ OPERATION**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B)
</dt> <dt>



La operación era ambigua.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**INFRACCIÓN DE CUOTA DE WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C)
</dt> <dt>



WMI está tomando demasiada memoria. Esto puede deberse a una baja disponibilidad de memoria o a un consumo excesivo de memoria por parte de WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM \_ E \_ TRANSACTION \_ CONFLICT**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D)
</dt> <dt>



La operación provocó un conflicto de transacción.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM \_ E \_ FORCED \_ ROLLBACK**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E)
</dt> <dt>



La transacción forzó una reversión.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM \_ E CONFIGURACIÓN REGIONAL NO \_ \_ ADMITIDA**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F)
</dt> <dt>



No se admite la configuración regional usada en la llamada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E \_ HANDLE \_ OUT \_ OF \_ DATE**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



El identificador de objeto no está actualizado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**ERROR DE CONEXIÓN WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



Error de conexión a la SQL de datos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM \_ E SOLICITUD DE IDENTIFICADOR NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



La solicitud de identificador no era válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM \_ E \_ PROPERTY \_ NAME \_ TOO \_ WIDE**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



El nombre de propiedad contiene más de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM \_ E \_ CLASS \_ NAME \_ TOO \_ WIDE**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



El nombre de clase contiene más de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM E METHOD NAME TOO WIDE (NOMBRE DEL MÉTODO WBEM \_ E \_ DEMASIADO \_ \_ \_ ANCHO)**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



El nombre del método contiene más de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM E QUALIFIER NAME TOO WIDE (NOMBRE DE CALIFICADOR WBEM \_ E \_ DEMASIADO \_ \_ \_ ANCHO)**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



El nombre del calificador contiene más de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM \_ E \_ RERUN \_ (COMANDO)**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



El SQL debe volver a ejecutarse porque hay un interbloqueo en SQL. Esto solo se puede devolver cuando los datos se almacenan en una base de SQL datos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM \_ E \_ DATABASE \_ VER \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



La versión de la base de datos no coincide con la versión que procesa el controlador del repositorio.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ VETO \_ DELETE**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



WMI no puede ejecutar la operación de eliminación porque el proveedor no la permite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ VETO \_ PUT**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A)
</dt> <dt>



WMI no puede ejecutar la operación put porque el proveedor no la permite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM \_ E CONFIGURACIÓN REGIONAL NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



El identificador de configuración regional especificado no era válido para la operación.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM \_ E \_ PROVIDER \_ SUSPENDED**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



El proveedor está suspendido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**SE REQUIERE SINCRONIZACIÓN \_ WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



El objeto debe escribirse en el repositorio WMI y recuperarse de nuevo para que la operación solicitada pueda realizarse correctamente. Esta constante se devuelve cuando un objeto debe estar confirmado y recuperado para ver el valor de propiedad.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ NO \_ SCHEMA**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



No se puede completar la operación; no hay ningún esquema disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM \_ E \_ PROVIDER \_ ALREADY \_ REGISTERED**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010)
</dt> <dt>



El proveedor no se puede registrar porque ya está registrado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM \_ E \_ PROVIDER \_ NOT \_ REGISTERED**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



El proveedor no se registró.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM \_ E \_ FATAL \_ TRANSPORT \_ ERROR**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Se produjo un error de transporte grave.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM \_ E \_ ENCRYPTED \_ CONNECTION \_ REQUIRED**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



El usuario intentó establecer un nombre de equipo o dominio sin una conexión cifrada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**TIEMPO DE \_ ESPERA DEL \_ PROVEEDOR WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Un proveedor no pudo notificar los resultados dentro del tiempo de espera especificado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ NO \_ KEY**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



El usuario intentó colocar una instancia sin clave definida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM \_ E \_ PROVIDER \_ DISABLED**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A)
</dt> <dt>



El usuario intentó registrar una instancia de proveedor, pero se descargó el servidor COM para la instancia del proveedor.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS \_ E \_ REGISTRATION \_ TOO \_ BROAD**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



El registro del proveedor se superpone con el dominio de eventos del sistema.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ E \_ REGISTRATION \_ TOO \_ PRECISE**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



No se utilizó una cláusula WITHIN en esta consulta.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ AUTHZ \_ NOT \_ PRIVILEGED**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



Este equipo no tiene los permisos de dominio necesarios para admitir las funciones de seguridad relacionadas con la instancia de suscripción creada. Póngase en contacto con el administrador de dominio para agregar este equipo al Windows de acceso de autorización.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ RETRY \_ LATER**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**CONTENCIÓN DE \_ RECURSOS \_ WBEM E \_**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ EXPECTED \_ QUALIFIER \_ NAME**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Se esperaba un nombre de calificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ EXPECTED \_ SEMI**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Punto y coma esperado o "=".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ EXPECTED \_ OPEN \_ BRACE**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Se esperaba una llave de apertura.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ EXPECTED \_ CLOSE \_ BRACE**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Falta la llave de cierre o un elemento de matriz no es posible.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**CORCHETE DE CIERRE ESPERADO DE WBEMMOF \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



Se esperaba un corchete de cierre.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ EXPECTED \_ CLOSE \_ PAREN**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Paréntesis de cierre esperados.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E VALOR CONSTANTE NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Valor numérico fuera del intervalo o cadenas sin comillas.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ EXPECTED \_ TYPE \_ IDENTIFIER**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



Se esperaba un identificador de tipo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ EXPECTED \_ OPEN \_ PAREN**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



Se esperaba un paréntesis abierto.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E TOKEN NO \_ \_ RECONOCIDO**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A)
</dt> <dt>



Token inesperado en el archivo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ UNRECOGNIZED \_ TYPE**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Identificador de tipo no reconocido o no admitido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ EXPECTED \_ PROPERTY \_ NAME**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Nombre de propiedad o método esperado.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF \_ E \_ TYPEDEF NO SE \_ \_ ADMITE**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D)
</dt> <dt>



No se admiten definiciones de tipos ni tipos enumerados.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**ALIAS INESPERADO DE WBEMMOF \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E)
</dt> <dt>



Solo una referencia a un objeto de clase puede tener un valor de alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ UNEXPECTED \_ ARRAY \_ INIT**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F)
</dt> <dt>



Inicialización de matriz inesperada. Las matrices deben declararse con \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ SINTAXIS DE MODIFICACIÓN NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



La sintaxis de ruta de acceso del espacio de nombres no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E MODIFICACIÓN DUPLICADA NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Especificadores de modificación duplicados.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ \_ PRAGMA NO VÁLIDA**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



[ \# pragma debe](pragma-namespace.md) ir seguido de una palabra clave válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ SINTAXIS DE ESPACIO DE NOMBRES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



La sintaxis de ruta de acceso del espacio de nombres no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ EXPECTED \_ CLASS \_ NAME**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



El carácter inesperado en el nombre de clase debe ser un identificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF \_ E \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



El valor especificado no se puede convertir en el tipo adecuado.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ EXPECTED \_ ALIAS \_ NAME**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



El signo de dólar debe ir seguido de un nombre de alias como identificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E DECLARACIÓN DE CLASE NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



La declaración de clase no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E DECLARACIÓN DE INSTANCIA NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



La declaración de instancia no es válida. Debe comenzar con "instancia de".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ EXPECTED \_ DOLLAR**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



Signo de dólar esperado. Un alias con el formato "$name" debe seguir la palabra clave "as".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**CALIFICADOR WBEMMOF \_ E \_ CIMTYPE \_**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A)
</dt> <dt>



El calificador "CIMTYPE" no se puede especificar directamente en un archivo MOF. Use la notación de tipo estándar.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ DUPLICATE \_ PROPERTY**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B)
</dt> <dt>



Se encontró un nombre de propiedad duplicado en el MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ ESPECIFICACIÓN DE ESPACIO DE NOMBRES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C)
</dt> <dt>



La sintaxis del espacio de nombres no es válida. No se permiten referencias a otros servidores.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E FUERA DEL \_ \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D)
</dt> <dt>



Valor fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ E ARCHIVO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E)
</dt> <dt>



El archivo no es un archivo MOF de texto válido o un archivo MOF binario.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**ALIAS DE WBEMMOF \_ E \_ EN \_ \_ EMBEDDED**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F)
</dt> <dt>



Los objetos incrustados no pueden ser alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ NULL \_ ARRAY \_ ELEM**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



No se admiten los elementos NULL de una matriz.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**CALIFICADOR DUPLICADO DE WBEMMOF \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



El calificador se usó más de una vez en el objeto .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ EXPECTED \_ FLAVOR \_ TYPE**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



Se esperaba un tipo de tipo como **ToInstance**, **ToSubClass,** **EnableOverride** o **DisableOverride.**


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**TIPOS DE TIPOS \_ \_ \_ INCOMPATIBLES \_ DE WBEMMOF E**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



La combinación **de EnableOverride** **y DisableOverride** en el mismo calificador no es legal.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ VARIOS \_ ALIAS**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Un alias no se puede usar dos veces.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E TIPOS DE TIPOS DE TIPOS \_ \_ \_ INCOMPATIBLES2**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



La combinación **de Restricted** y **ToInstance** o **ToSubClass** no es legal.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E NO SE \_ \_ DEVUELVEN \_ MATRICES**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



Los métodos no pueden devolver valores de matriz.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E DEBE ESTAR DENTRO O \_ \_ \_ \_ \_ FUERA**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Los argumentos deben tener un **calificador In** **u Out.**


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ SINTAXIS DE MARCAS NO \_ \_ VÁLIDAS**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



La sintaxis de marcas no es válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E \_ EXPECTED \_ BRACE \_ OR \_ BAD \_ TYPE**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



Faltan la llave final y el punto y coma de una clase.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E VALOR DE CALIDAD \_ \_ CIMV22 \_ NO \_ ADMITIDO**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A)
</dt> <dt>



No se admite una característica cim versión 2.2 para un valor calificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**TIPO DE DATOS \_ \_ \_ CIMV22 \_ \_ NO ADMITIDO DE WBEMMOF E**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B)
</dt> <dt>



No se admite el tipo de datos CIM versión 2.2.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ SINTAXIS \_ DELETEINSTANCE NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C)
</dt> <dt>



La sintaxis de la instancia de eliminación no es válida. Debe ser `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ SINTAXIS DE \_ CALIFICADOR NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D)
</dt> <dt>



La sintaxis del calificador no es válida. Debería ser `qualifiername:type=value,scope(class|instance), flavorname`.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**CALIFICADOR WBEMMOF \_ E USADO FUERA DEL \_ \_ \_ \_ ÁMBITO**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E)
</dt> <dt>



El calificador se usa fuera de su ámbito.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**ERROR DE WBEMMOF \_ E AL CREAR UN ARCHIVO \_ \_ \_ \_ TEMPORAL**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F)
</dt> <dt>



Error al crear el archivo temporal. El archivo temporal es una fase intermedia de la compilación MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF \_ E \_ ERROR \_ INVALID \_ INCLUDE \_ FILE**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Un archivo incluido en el MOF por el comando de preprocesador [ \# include](-include.md) no es válido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ SINTAXIS \_ DELETECLASS NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



La sintaxis de los comandos de preprocesador [ \# pragma deleteinstance](pragma-deleteinstance.md) o [ \# pragma deleteclass](pragma-deleteclass.md) no es válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>WbemCli.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WbemCli.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de retorno wmi](wmi-return-codes.md)
</dt> </dl>

 

