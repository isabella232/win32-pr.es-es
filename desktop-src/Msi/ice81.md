---
description: ICE81 valida la tabla MsiDigitalCertificate, la tabla MsiDigitalSignature, la tabla MsiPatchCertificate y la tabla MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074530"
---
# <a name="ice81"></a>ICE81

ICE81 valida la tabla [MsiDigitalCertificate,](msidigitalcertificate-table.md)la tabla [MsiDigitalSignature,](msidigitalsignature-table.md) [la tabla MsiPatchCertificate](msipatchcertificate-table.md)y la [tabla MsiPackageCertificate](msipackagecertificate-table.md). Esta acción personalizada de ICE publica advertencias para los certificados digitales que no se usan o no se referencian, y publica un error cuando el objeto firmado no existe o cuando el gabinete del objeto firmado no apunta a datos externos.

Tenga en cuenta que ICE03 comprueba que la entrada de la columna Tabla de la tabla MsiDigitalSignature es "Media".

## <a name="result"></a>Resultado

ICE81 publica las siguientes advertencias para certificados digitales sin usar o sin referencia.



| Advertencia de ICE81                                                                                                                                                      | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| No se puede encontrar ninguna referencia a ninguno de los registros de la tabla MsiDigitalCertificate en las tablas MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate. | Esta advertencia se devuelve si no se usan todos los registros.                |
| No se encontró ninguna referencia al certificado digital 1 en las tablas \[ \] MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.                         | Esta advertencia se devuelve si algunos registros, pero no todos, no se usan. |



 

ICE81 publica los siguientes errores.



| Error ice81                                                                                                                                                              | Descripción                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabla multimedia no existe. Por lo tanto, todas las entradas de MsiDigitalSignature son incorrectas                                                                                   | El objeto con firma no existe. Este error se devuelve si la tabla Media no existe pero MsiDigitalSignature tiene entradas.                                |
| Falta el objeto con firma \[ 2 \] en la tabla multimedia                                                                                                                               | El objeto \[ con firma 2 no \] existe. Este error se devuelve si existe la tabla Media, pero esta entrada de MsiDigitalSignature no está presente en la tabla Media. |
| La entrada de la \[ tabla 1 \] con la clave \[ 2 está \] firmada. Por lo tanto, el gabinete debe apuntar a un objeto fuera del paquete (el valor de Gabinete NO debe tener el prefijo \# ) | El gabinete del objeto firmado no apunta a datos externos. \[1 \] es el nombre de la tabla. \[2 \] es clave en la tabla Multimedia.                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



