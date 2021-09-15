---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476509"
---
# <a name="cert2spc"></a>Cert2SPC

La herramienta Cert2SPC crea una prueba [*de Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) mediante certificados [*X.509*](../secgloss/x-gly.md) [*existentes.*](../secgloss/c-gly.md) Cert2SPC puede encapsular varios certificados X.509 en un objeto de datos firmados [*PKCS \# 7.*](../secgloss/p-gly.md) La herramienta se instala en la carpeta Bin de la ruta de instalación del Kit de desarrollo de software \\ (SDK) de Microsoft Windows.

Cert2SPC está disponible como parte del SDK Windows, que puede descargar de <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Esta herramienta solo tiene fines de prueba. Se obtiene un SPC válido de una entidad [*de certificación.*](../secgloss/c-gly.md)


**Cert2SPC** *Cert1.cer Cert2.cer* ... *Output.spc*

 



| Parámetros              | Descripción                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1.cer Cert2.cer* ... | Nombres de los certificados X.509 que se incluirán en el SPC. Cada nombre de certificado termina con la extensión .cer.                         |
| *Output.spc*            | Nombre del objeto PKCS \# 7 que contiene los certificados X.509 que se crearán. El nombre del archivo de salida termina con la extensión .spc. |



 

 

 
