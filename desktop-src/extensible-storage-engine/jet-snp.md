---
description: 'Más información sobre: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474131"
---
# <a name="jet_snp"></a>JET_SNP


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_snp"></a>JET_SNP

El **JET_SNP** de constantes describe el tipo de la operación para la que se va a obtener información de progreso. Estas constantes se usan como parámetro *snp* de [la](./jet-pfnstatus-callback-function.md) JET_PFNSTATUS de devolución de llamada.


| <p>Constante o valor</p> | <p>Descripción</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>La devolución de llamada es para una operación de reparación.</p> | 
| <p>JET_snpCompact<br />4</p> | <p>La devolución de llamada es para la desfragmentación de la base de datos.</p> | 
| <p>JET_snpRestore<br />8</p> | <p>La devolución de llamada es para una operación de restauración.</p> | 
| <p>JET_snpBackup<br />9</p> | <p>La devolución de llamada es para una operación de copia de seguridad.</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>No se admite.</p><p><strong>Windows 2000:</strong>  La devolución de llamada es para la operación de actualización de formato de base de datos.</p> | 
| <p>JET_snpScrub<br />11</p> | <p>La devolución de llamada es para una operación de ceros de base de datos (es decir, limpieza).</p><p><strong>Windows Server 2003 y Windows 2000 Server:</strong>  No se admite.</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>La devolución de llamada es para el proceso de actualización del formato de registro de todas las páginas de base de datos.</p><p><strong>Windows Server 2003 y Windows 2000 Server:</strong>  No se admite.</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
