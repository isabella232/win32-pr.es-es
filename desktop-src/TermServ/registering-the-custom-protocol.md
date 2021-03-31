---
title: Registro del administrador de protocolos
description: Debe crear al menos una entrada de valor de registro para el administrador de protocolos para que el servicio de Servicios de Escritorio remoto pueda crear una instancia de ella.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418522"
---
# <a name="registering-the-protocol-manager"></a>Registro del administrador de protocolos

Debe crear al menos una entrada de valor de registro para el administrador de protocolos para que el servicio de Servicios de Escritorio remoto pueda crear una instancia de ella.

## <a name="registry-location"></a>Ubicación del registro

Cree una clave del registro en la siguiente ubicación para cada agente de escucha ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que usa el protocolo. En este ejemplo, las nuevas claves de agente de escucha se denominan *MyListener1* y *MyListener2*.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

Como referencia, puede ver las entradas de valor en la clave de escucha **RDP-TCP** predeterminada en esta ubicación.

## <a name="registry-value-entries"></a>Entradas de valores del registro

La clave del agente de escucha para el protocolo debe tener una entrada de valor denominada **\_ objeto LoadableProtocol**<dl> <dt>

Tipo de datos
</dt> <dd>REG_SZ</dd> Interfaz </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> ). El servicio Servicios de Escritorio remoto usa este CLSID para crear una instancia del administrador de protocolos para este agente de escucha después de encontrar el agente de escucha en el registro.

Si el proveedor de protocolo usa más de un agente de escucha, el servicio Servicios de Escritorio remoto solo crea una instancia del administrador de protocolos y la usa para llamar a [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) una vez para cada agente de escucha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un proveedor de Protocolo de escritorio remoto](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Secuencia de llamada al método](method-call-sequence.md)
</dt> </dl>

 

 




