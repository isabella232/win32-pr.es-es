---
title: Configuración del complemento del servicio WinRM
description: Un Windows de administración remota (WinRM) debe estar registrado en el catálogo de WinRM para permitir que la infraestructura determine dinámicamente el conjunto de complementos disponibles y los URI de recursos que admiten.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b82b24b8631cd6a47a879a6fa0684b9b2ac9c542699396d0f0997afe14cac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323732"
---
# <a name="winrm-service-plug-in-configuration"></a>Configuración del complemento del servicio WinRM

Un Windows de administración remota (WinRM) debe estar registrado en el catálogo de WinRM para permitir que la [](windows-remote-management-glossary.md) infraestructura determine dinámicamente el conjunto de complementos disponibles y los URI de recursos que admiten. Todos [*los URI de*](windows-remote-management-glossary.md) recursos para los complementos de WinRM deben ajustarse al formato definido en RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ). La configuración se realiza a través del servicio WinRM principal.

El siguiente comando registra una configuración de complemento con el servicio WinRM:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> El servicio WinRM debe reiniciarse para exponer los complementos recién registrados.

La configuración del complemento se especifica en XML. A continuación se muestra un ejemplo.

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



En la lista siguiente se describen los elementos XML con más detalle y va seguido del esquema de configuración especificado como XSD.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**
</dt> <dd>

Especifica el nombre de archivo del complemento de operaciones. Las variables de entorno que se coloquen en esta entrada se expandirán en el contexto de los usuarios cuando llegue una solicitud. Cada usuario podría tener una versión diferente de la misma variable de entorno, por lo que cada usuario podría terminar con un complemento diferente. Esta entrada no puede estar en blanco y debe apuntar a un complemento válido.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nombre**
</dt> <dd>

Especifica el nombre para mostrar que se usará para el complemento. Si se devuelve un error desde el complemento, este nombre se colocará en el XML de error que se devuelve a la aplicación cliente. El nombre no es específico de la configuración regional.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Arquitectura**
</dt> <dd>

Especifica si el complemento de operaciones es de 32 o 64 bits. Si no se especifica este elemento, el valor predeterminado será "32" en sistemas x86 y en "64" en sistemas de 64 bits. Para los sistemas x86, el único valor válido es "32". Si el valor es "32" en un sistema de 64 bits, debe tenerse en cuenta el redireccionamiento wow64 al escribir la información **de nombre de** archivo. El sistema de archivos subyacente usará el redireccionamiento wow64 para traducir system32 a syswow64. Por ejemplo, si **Filename** es "%windir% system32myplugin.dll" y Architecture es "32", el archivo de complemento real se encuentra en \\ \\  "%windir% \\ syswow64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**
</dt> <dd>

Configura el formato en el que xml se pasa a los complementos a través del [**objeto \_ DATA de WSMAN.**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) Los siguientes tipos están disponibles:

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Los datos XML entrantes están contenidos en una estructura TEXT de tipo de datos de WSMAN, que representa el XML como \_ \_ búfer de memoria \_ **PCWSTR.**

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Xmlreader
</dt> <dd>

Los datos XML entrantes se encuentran en una estructura WSMAN DATA TYPE WS XML READER, que representa el XML como un objeto XmlReader, que se define en el archivo de encabezado \_ \_ \_ \_ \_ WebServices.h. 

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**
</dt> <dd>

Este nodo es opcional y permite que un complemento configure XML adicional que se pasará al [**método WSManPluginStartup.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup) La mayoría de los complementos no necesitarán esta información adicional, pero si es necesario usar un complemento en más de un escenario que requiera una semántica en tiempo de ejecución diferente, este XML dará al complemento la flexibilidad necesaria para ello.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Recursos**
</dt> <dd>

Especifica una lista de [*identificadores URI de*](windows-remote-management-glossary.md)recursos que admite este complemento. Se debe especificar al menos una entrada **ResourceUri;** De lo contrario, se rechazará el XML.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Recursos** / **Recurso**
</dt> <dd>

Representa una configuración de [*URI de recurso*](windows-remote-management-glossary.md)único.

> [!Note]  
> El **atributo SupportsOptions** se puede establecer en false. Si **SupportsOptions se** establece en false, este atributo no aparece cuando se enumera el recurso.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Recursos** / **Recurso** / **ResourceUri**
</dt> <dd>

Especifica un único [*URI de recurso*](windows-remote-management-glossary.md) completo o como una cadena de coincidencia parcial basada en el atributo **ExactMatch.** Si **ExactMatch** no está presente, el valor predeterminado es **False**, lo que significa que el procesador SOAP de WinRM hará una coincidencia parcial con el inicio del *URI* del recurso y, si hay una coincidencia, la pasará al complemento. El **atributo SupportsOptions** se puede especificar si este *URI* de recurso puede tener alguna opción pasada. De forma predeterminada, no se admite ninguna opción y, si hay alguna en la solicitud de cliente, se devolverá un error. Si el complemento admite opciones, es importante que el complemento devuelva el error correcto si hay una opción que el complemento no entiende cuando la marca **mustUnderstand** está establecida en **True.**

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Recursos** / **Recurso** / **Funcionalidad**
</dt> <dd>

Especifica una funcionalidad que está disponible en este [*URI de recurso.*](windows-remote-management-glossary.md) Habrá una entrada para cada tipo de operación que admita. Están disponibles las opciones siguientes:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Obtener
</dt> <dd>

Las operaciones get se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** se usa si la operación get admite el concepto . El **atributo SupportFiltering** no es válido y debe establecerse en false. Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Poner
</dt> <dd>

Las operaciones put se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** se usa si la operación put admite el concepto . El **atributo SupportFiltering** no es válido y debe establecerse en **False.** Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Crear
</dt> <dd>

Las operaciones de creación se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** se usa si la operación de creación admite el concepto . El **atributo SupportFiltering** no es válido y debe establecerse en **False.** Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Eliminar
</dt> <dd>

Las operaciones de eliminación se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** se usa si la operación de eliminación admite el concepto . El **atributo SupportFiltering** no es válido y debe establecerse en **False.** Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invocar
</dt> <dd>

Las operaciones de invocación se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** no se admite para las operaciones de invocación y debe establecerse en false. El **atributo SupportFiltering** no es válido y debe establecerse en **False.** Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerar
</dt> <dd>

Las operaciones enumeradas se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** no se admite para las operaciones de enumeración y debe establecerse en **False.** El **atributo SupportFiltering** es válido y, si el complemento admite el filtrado de este atributo, debe establecerse en **True.** Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>subscribir
</dt> <dd>

Las operaciones de suscripción se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment no** se admite para las operaciones de suscripción y debe establecerse en **False.** El **atributo SupportFiltering** no es válido y debe establecerse en **False.** Esta funcionalidad no es válida para un *URI de* recurso si también se admiten operaciones de shell.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Cáscara
</dt> <dd>

Las operaciones de shell se admiten en el [*URI del recurso.*](windows-remote-management-glossary.md) El **atributo SupportFragment** no se admite para las operaciones de shell y debe establecerse en **False.** El **atributo SupportFiltering** no es válido y debe establecerse en **False.** Esta funcionalidad no es válida para un *URI de recurso* si también se admite cualquier otra funcionalidad de operación. Si se configura una funcionalidad de operación de shell para un *URI* de recurso, las operaciones get, put, create, delete, invoke y enumerate se procesan internamente en el servicio WinRm para administrar shells. Como resultado, el complemento no puede tratar con las propias operaciones.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Recursos** / **Recurso** / **Seguridad**
</dt> <dd>

Este elemento define el descriptor de seguridad (a través del atributo **Sddl)** que se debe aplicar para determinar el acceso a un [*URI*](windows-remote-management-glossary.md) de recurso determinado (a través del **atributo URI).** Si **ExactMatch** no está presente, el elemento **Security** tiene como valor predeterminado  **False**, lo que significa que **sddl** se aplica a todos los URI de recursos que comparten **uri** como prefijo. Si **ExactMatch** se establece en true, **sddl** solo se aplica al **URI** exacto especificado. Si hay varias entradas **de** seguridad que podrían aplicarse a un *URI* de recurso determinado, se usa la coincidencia de prefijo más larga para determinar el **sddl adecuado.** Como resultado de la coincidencia de prefijo más larga, si existe una entrada **uri** de coincidencia exacta, siempre se elegirá como el elemento Security adecuado.

</dd> </dl>

A continuación se muestra el esquema de configuración del complemento especificado como XSD.

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




