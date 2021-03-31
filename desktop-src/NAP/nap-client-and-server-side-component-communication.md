---
title: Comunicación de componentes del lado servidor y del cliente NAP
description: Comunicación de componentes del lado servidor y del cliente NAP
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419050"
---
# <a name="nap-client-and-server-side-component-communication"></a>Comunicación de componentes del lado servidor y del cliente NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El componente agente NAP puede comunicarse con el componente de servidor de administración de NAP a través del proceso siguiente:

1.  El agente NAP pasa el SSoH a NAP EC.
2.  El NAP EC pasa el SSoH a NAP.
3.  NAP ES pasa el SSoH al servicio del servidor de directivas de redes (NPS).
4.  El servicio NPS pasa el SSoH al servidor de administración de NAP.

Un SHA puede comunicarse con su SHV correspondiente a través del proceso siguiente:

1.  SHA pasa su SoH al agente NAP.
2.  El agente NAP pasa el SoH, contenido dentro de SSoH, al NAP EC.
3.  El NAP EC pasa el SoH a NAP.
4.  NAP ES el que pasa el SoH al servidor de administración de NAP.
5.  El servidor de administración de NAP pasa el SoH al SHV.

En la siguiente ilustración se muestra el proceso de comunicación de los componentes del cliente de NAP a los componentes del lado servidor NAP.

![arquitectura de la comunicación de cliente a servidor en la plataforma NAP](images/nap-client-to-server-comm.png)

El servidor de administración de NAP puede comunicarse con el agente NAP a través del proceso siguiente:

1.  El servidor de administración de NAP pasa el SoHRs al servicio NPS.
2.  El servicio NPS pasa el SSoHR a NAP ES.
3.  NAP ES pasa el SSoHR a NAP EC.
4.  El NAP EC pasa el SSoHR al agente NAP.

El SHV puede comunicarse con su SHA correspondiente a través del proceso siguiente:

1.  El SHV pasa su SoHR al servidor de administración de NAP.
2.  El servidor de administración de NAP pasa el SoHR al servicio NPS.
3.  El servicio NPS pasa el SoHR, contenido dentro de SSoHR, a NAP ES.
4.  NAP ES pasa el SoHR a NAP EC.
5.  El NAP EC pasa el SoHR al agente NAP.
6.  El agente NAP pasa el SoHR al SHA.

En la siguiente ilustración se muestra el proceso de comunicación de los componentes del lado servidor NAP a los componentes del cliente de NAP.

![arquitectura de la comunicación de servidor a cliente en la plataforma NAP](images/nap-server-to-client-comm.png)

 

 




