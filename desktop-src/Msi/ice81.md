---
description: ICE81 valida la tabla MsiDigitalCertificate, la tabla MsiDigitalSignature, la tabla MsiPatchCertificate y la tabla MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810742"
---
# <a name="ice81"></a>ICE81

ICE81 valida la tabla [MsiDigitalCertificate](msidigitalcertificate-table.md), la tabla [MsiDigitalSignature](msidigitalsignature-table.md), la tabla [MsiPatchCertificate](msipatchcertificate-table.md)y la [tabla MsiPackageCertificate](msipackagecertificate-table.md). Esta acción personalizada de ICE publica advertencias para los certificados digitales que no se usan o a los que no se hace referencia, y envía un error cuando el objeto firmado no existe o cuando el archivo. cab del objeto firmado no apunta a datos externos.

Tenga en cuenta que ICE03 comprueba que la entrada de la columna de tabla de la tabla MsiDigitalSignature es "media".

## <a name="result"></a>Resultado

ICE81 envía las siguientes advertencias para los certificados digitales no usados o sin referencia.



| ADVERTENCIA de ICE81                                                                                                                                                      | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| No se encontró ninguna referencia a ninguno de los registros de la tabla MsiDigitalCertificate en las tablas MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate. | Se devuelve esta advertencia si no se utilizan todos los registros.                |
| No se encontró ninguna referencia al certificado digital \[ 1 \] en las tablas MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.                         | Se devuelve esta advertencia si no se usan algunos registros, pero no todos. |



 

ICE81 expone los siguientes errores.



| Error ICE81                                                                                                                                                              | Descripción                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabla de medios no existe. Por lo tanto, todas las entradas de MsiDigitalSignature son incorrectas                                                                                   | El objeto firmado no existe. Se devuelve este error si la tabla de medios no existe pero MsiDigitalSignature tiene entradas.                                |
| Falta el objeto con signo \[ 2 \] en la tabla de medios                                                                                                                               | El objeto con signo \[ 2 no \] existe. Este error se devuelve si la tabla de medios existe, pero esta entrada en MsiDigitalSignature no está presente en la tabla de medios. |
| La entrada de la tabla \[ 1 \] con la clave \[ 2 \] está firmada. Por lo tanto, el archivo. cab debe apuntar a un objeto fuera del paquete (el valor de Cabinet no debe ir precedido de \# ) | El archivo. cab del objeto firmado no apunta a datos externos. \[1 \] es el nombre de la tabla. \[2 \] es la clave en la tabla de medios.                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



