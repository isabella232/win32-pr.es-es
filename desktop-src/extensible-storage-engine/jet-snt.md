---
description: 'Más información sobre: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 250ad992ec26b218bab21691f26c0938b6be6921
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481391"
---
# <a name="jet_snt"></a>JET_SNT


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_snt"></a>JET_SNT

El [JET_SNT]() de constantes describe los puntos del progreso de una operación sobre qué [](./jet-pfnstatus-callback-function.md) información se solicita en una llamada a la función de devolución JET_PFNSTATUS llamada.


| <p>Constante o valor</p> | <p>Descripción</p> | 
|-----------------------|--------------------|
| <p>JET_sntBegin<br />5</p> | <p>El principio de una operación</p> | 
| <p>JET_sntRequirements<br />7</p> | <p>No se admite.</p><p><strong>Windows 2000 Server:</strong>  Se inicia la operación. En este caso, el último parámetro de la función de devolución de llamada debe ser un puntero válido a una <a href="gg269328(v=exchg.10).md">estructura JET_SNPROG</a> que indica el número total de unidades que se ejecutarán.</p> | 
| <p>JET_sntProgress<br />0</p> | <p>El número de unidades completadas y el número de unidades aún por realizar. Esta información se devuelve en los miembros de una <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> estructura.</p> | 
| <p>JET_sntComplete<br />6</p> | <p>La finalización de una operación.</p> | 
| <p>JET_sntFail<br />3</p> | <p>Error de una operación.</p> | 
| <p>JET_sntRecoveryStep<br />8</p> | <p>Control de recuperación de una operación.</p><div class="alert">&gt; [!NOTE]&gt; <P>Este valor no es aplicable a las versiones del sistema operativo Windows a partir de Windows 8.</P></div> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
