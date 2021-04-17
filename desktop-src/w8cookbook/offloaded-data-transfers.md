---
title: Transferencias de datos descargados
description: Transferencias de datos descargados
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- descarga de copia
- reduce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105714487"
---
# <a name="offloaded-data-transfers"></a>Transferencias de datos descargados

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

Para hacer avanzar el movimiento de datos de almacenamiento, Microsoft ha desarrollado una nueva tecnología de transferencia de datos: transferencia de datos descargados (ODX). En lugar de usar operaciones de lectura y escritura almacenadas en búfer, Windows ODX inicia la operación de copia con una descarga leída y recupera un token que representa los datos del dispositivo de almacenamiento y, a continuación, usa un comando de carga de descarga con el token para solicitar el movimiento de datos del disco de origen al disco de destino. El administrador de copia de los dispositivos de almacenamiento realiza el movimiento de datos según el token. En Windows 8, el administrador de ti y el administrador de almacenamiento pueden usar la característica ODX de Windows para interactuar con el dispositivo de almacenamiento con el fin de trasladar archivos o datos de gran tamaño a través de la red de almacenamiento de alta velocidad. Windows ODX reducirá notablemente el tráfico de red de cliente-servidor y el uso de tiempo de CPU durante las transferencias de datos grandes porque todo el movimiento de datos se encuentra en la red de almacenamiento de back-end. ODX se puede usar en la implementación de máquinas virtuales, la migración de datos masiva y la compatibilidad con dispositivos de almacenamiento en capas, y puede reducir el costo de la implementación de hardware físico a través de las características de almacenamiento ODX y de aprovisionamiento fino.

> [!Note]  
> Esta característica solo funcionará en dispositivos de almacenamiento con la implementación de la especificación de SPC4 y SBC3.

 

## <a name="functional-details"></a>Detalles funcionales

-   La característica ODX de Windows se incrusta en el motor de copia del sistema operativo Windows. durante la enumeración de almacenamiento, Windows consultará la funcionalidad ODX del dispositivo de almacenamiento.
-   Copiar el dispositivo de almacenamiento de origen y el dispositivo de almacenamiento de destino de copia deben administrarse en el mismo administrador de copias para admitir la descarga de copia
-   Si se produce un error en una operación de descarga de copia, el administrador de copias del dispositivo de almacenamiento debe devolver los datos de detección adicionales adecuados para el control de errores de las aplicaciones.
-   El motor de copia de Windows revertirá a la operación de copia tradicional si se produce un error en la operación de descarga de copia

## <a name="using-odx"></a>Usar ODX

-   La aplicación de transferencia de datos debe asegurarse de que tanto el LUN de origen de copia como el LUN de destino de copia son compatibles con ODX antes de llamar a las rutinas de la API ODX
-   En el explorador de Windows, los usuarios pueden usar "arrastrar" o "copiar y pegar" para realizar la descarga de copia
-   Cuando el LUN de origen y el LUN de destino se montan con el sistema de archivos, la aplicación solo debe llamar a la descarga \_ \_ de fsctl y la \_ \_ escritura de descarga de fsctl para realizar la transferencia de datos desde el LUN de origen al LUN de destino.
-   Si se produce un error en una operación de descarga de copia, el administrador de copias del dispositivo de almacenamiento debe devolver los datos de detección adicionales adecuados para el control de errores de las aplicaciones.
-   Cuando el LUN de origen o el LUN de destino no están montados con el sistema de archivos y están bloqueados, la aplicación debe llamar al almacenamiento de IOCTL \_ \_ administrar \_ \_ \_ los atributos del conjunto de datos con la \_ acción DeviceDsmAction OffloadRead o DeviceDsmAction \_ OffloadWrite para realizar la descarga de la copia.
-   Las aplicaciones de administración de almacenamiento pueden usar la \_ \_ API de paso a través de SCSI para realizar transferencias de datos descargados si los LUN de origen y de destino no se montan con ningún sistema de archivos y están bloqueados.

## <a name="tests"></a>Pruebas

-   Para garantizar una experiencia de usuario sólida, Compruebe la certificación de Windows ODX de la matriz de almacenamiento.
-   El dispositivo de almacenamiento debe cumplir los requisitos de certificación de las transferencias de datos descargados de Windows (que se usan como logotipo) para admitir la característica ODX
-   Use el kit de certificación de hardware de transferencias de datos descargados de Windows para comprobar la compatibilidad de las características de ODX con los dispositivos de almacenamiento

## <a name="resources"></a>Recursos

-   Especificación de la XCOPY XCOPY Lite (11-059r8)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [Servicios del panel de hardware](/windows-hardware/drivers/dashboard/)
-   [\_Estructura de paso \_ a través de SCSI](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 