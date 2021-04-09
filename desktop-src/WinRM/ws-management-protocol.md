---
title: Protocolo WS-Management
description: Estándar público para el intercambio remoto de datos de administración con cualquier dispositivo de equipo que implemente el protocolo.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149606"
---
# <a name="ws-management-protocol"></a>Protocolo WS-Management

El protocolo WS-Management fue desarrollado por un grupo de fabricantes de hardware y software como estándar público para el intercambio remoto de datos de administración con cualquier equipo que implemente dicho protocolo.

## <a name="standards"></a>Estándares

Para obtener más información sobre el protocolo de WS-Management, consulte [especificación de servicios web para administración (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

La intención del protocolo es proporcionar coherencia e interoperabilidad para las operaciones de administración en muchos tipos de dispositivos (incluido el firmware) y sistemas operativos. WS-Management Protocolo se puede extender a medida que el sector de ti identifica nuevas operaciones.

La implementación actual del Protocolo de WS-Management se basa en las siguientes especificaciones estándar: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration y WS-Eventing. Para obtener más información acerca de los estándares de WS-Management y los esquemas XML, vea. <https://dmtf.org/standards/wsman>

## <a name="messages"></a>error de Hadoop

El protocolo WS-Management proporciona un estándar para construir [*mensajes*](windows-remote-management-glossary.md) XML mediante varios estándares de servicios Web, como [*WS-Addressing*](windows-remote-management-glossary.md) y [*WS-Transfer*](windows-remote-management-glossary.md). Estos estándares definen esquemas XML para los mensajes del servicio Web. Los mensajes hacen referencia a un [*recurso*](windows-remote-management-glossary.md) mediante un [*URI de recurso*](windows-remote-management-glossary.md). El protocolo WS-Management agrega un conjunto de definiciones para las operaciones de administración y los valores. Por ejemplo, WS-Transfer define las operaciones de obtención, colocación, creación y eliminación de un recurso. WS-Management protocolo agrega Rename, Partial get y put parcial.

Los mensajes siguen las convenciones de [*Protocolo simple de acceso a objetos (SOAP)*](windows-remote-management-glossary.md) que usan todos los protocolos de servicios Web.

En el ejemplo de código siguiente se muestra un mensaje con una operación get. Este ejemplo se muestra como ayuda para comprender el aspecto de los mensajes subyacentes. No es necesario saber cómo generar mensajes SOAP. Los mensajes se ensamblan mediante Administración remota de Windows cuando se ejecuta un comando con la herramienta de línea de comandos **WinRM** o se ejecuta un script escrito con la [API de scripting de WinRM](winrm-scripting-api.md).

El mensaje es una solicitud para obtener la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con una propiedad **DeviceID** de "c:" de un servidor denominado equiporemoto. La solicitud utiliza el transporte HTTP a través del puerto 80. La cuenta que envía la solicitud debe estar en el grupo de administradores local en el equipo remoto.

Los caracteres situados delante de los dos puntos al principio de cada etiqueta indican qué estándar define el elemento XML. Por ejemplo, ` <wsa:To>` indica que el elemento to está definido por el estándar WS-Addressing e `<s:Header>` indica el principio del contenido del encabezado de un mensaje SOAP. Tenga en cuenta que la mayoría del mensaje se compone de elementos XML definidos por SOAP o WS-Addressing. WS-Management protocolo agrega MaxEnvelopeSize, selector y SelectorSet.


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Administración remota de hardware](remote-hardware-management.md)
</dt> </dl>

 

 